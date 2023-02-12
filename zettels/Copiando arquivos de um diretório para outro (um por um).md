tags: #programação/python/code 

```Python
import os
import shutil

HOME = os.path.expanduser('~')
PICTURES = os.path.join(HOME, 'Pictures')
PASTA_ORIGINAL = os.path.join(PICTURES, 'ai_images')
NOVA_PASTA = os.path.join(PICTURES, 'cópia_ai_images')

os.makedirs(NOVA_PASTA, exist_ok=True)

for root, dirs, files in os.walk(PASTA_ORIGINAL):
    for dir_ in dirs:
        caminho_novo_diretorio = os.path.join(
            root.replace(PASTA_ORIGINAL, NOVA_PASTA), dir_
        )
        os.makedirs(caminho_novo_diretorio, exist_ok=True)

    for file in files:
        caminho_arquivo = os.path.join(root, file)
        caminho_novo_arquivo = os.path.join(
            root.replace(PASTA_ORIGINAL, NOVA_PASTA), file
        )
        shutil.copy(caminho_arquivo, caminho_novo_arquivo)

```
- Primeiro começamos a declarar as constantes. Usando o "os.path.expanduser" pasando o "~" como parâmetro, conseguimos a home do sistema, que no caso é `c:\Users\luizh`.
- Em seguida, declaramos o caminho, a partir da home, da pasta onde queremos modificar.
- Utilizando o "os.makedirs", criamos a nova pasta, com o parâmetro nomeado "exists_ok=True" que, não da erro caso a pasta já foi criada.
- Iteramos o "os.walk" com as três variáveis padrão.
- Em seguida, iteramos os diretórios, para pegarmos o "caminho_novo_diretorio", dando um "os.join" passando o root com "replace" da nova pasta, e o próprio diretório. Ai chamamos o "os.makedirs" para criar a pasta com o caminho que pegamos.
- Por seguinte, iteramos os arquivos, para pegarmos o "caminho_arquivo", utilizando o "os.join", logo em seguida, copiamos o código a cima, mas agora em vez de passar o diretório, passamos o arquivo.
- Finalmente, utlizamos o módulo "shutil", nele usamos o método copy. Passamos os parâmetros do que vai ser copiado (caminho_arquivo) e logo após, passamos o caminho onde vai ser copiado (caminho_novo_arquivo).

# Reference
- [Curso de Python do Luiz Otávio Miranda](https://www.udemy.com/user/luiz-otavio-miranda)
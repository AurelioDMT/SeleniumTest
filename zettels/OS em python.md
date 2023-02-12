tags: #programação/python 
Doc: https://docs.python.org/3/library/os.html

# OS
- O módulo os (operation system), serve para a interação com seu sistema operacional.

## os.path
Doc: https://docs.python.org/3/library/os.path.html#module-os.path

- Serve para manipular caminhos no seu sistema operacional.

1.  Para criar caminhos:
```Python
caminho = os.path.join('Desktop', 'curso', 'arquivo.txt')
```

2. Para separar o diretório do arquivo:
```Python
diretorio, arquivo = os.path.split(caminho)
```

3. Para separar o arquivo e sua extenção:
```Python
nome_arquivo, extensao_arquivo = os.path.splitext(arquivo)
```

4. Para checar se o arquivo existe:
```Python
os.path.exists('C:\\Users\\luizh\\code\\POO Python')
```

5. Para pegar o útlimo arquivo em um caminho:
```Python
os.path.basename(caminho)
```

6. Para pegar todo o caminho, exeto o útimo:
```Python
os.path.dirname(caminho)
```

# os.listdir
- Nele você pode listar itens em uma pasta. Basta passar o caminho.
- Lembrando que para ele listar subpastas, você pode utilizar o nome retornado por "os.listdir" e dar um "os.path.join" no caminho e no nome do arquivo. Assim você conseguirá dar outro for, utilizando o "os.listdir":
```Python
import os

# r'C:\Users\luizh\Pictures'
caminho = os.path.join(r'c:\\Users\\', 'luizh', 'Pictures',)

for pasta in os.listdir(caminho):
    caminho_completo_pasta = os.path.join(caminho, pasta)
    print(pasta)

    if not os.path.isdir(caminho_completo_pasta):
        continue

    for imagem in os.listdir(caminho_completo_pasta):
        print('  ', imagem)
```
- Neste código, pegamos o path desejado, para dar um for nele.
- Pego o caminho completo de cada item.
- Printo a pasta.
- Checo se o arquivo é um diretório (pasta).
- Dou outro for nos diretórios dessa pasta, e mostro todos os items, indentados por cada pasta.

# os.walk
- Lista as pastas **recursivamente**, gera uma sequência de tuplas, onde cada tupla possui três elementos:
	1. root - o diretório atual.
	2. dirs -  uma lista de subdiretórios.
	3. files - uma lista dos arquivos do diretório atual.
```Python
import os
from itertools import count

# r'C:\Users\luizh\Pictures'
caminho = os.path.join(r'c:\\Users\\', 'luizh', 'Pictures')
counter = count()

for root, dirs, files in os.walk(caminho):
    the_counter = next(counter)
    print(the_counter, 'Pasta atual: ', root)

    for dir_ in dirs:
        print('  ', the_counter, 'Dir: ', dir_)

    for file_ in files:
        print('  ', the_counter, 'Dir: ', file_)

```

# os.stat
Doc: https://docs.python.org/3/library/os.html#os.stat

- Pega o status de um arquivo.
- Retorna um objeto "stat_result".
- Com isso, podemos pegar o tamanho de arquivos, datas de modificações, datas de criação do arquivo etc.
```Python
import math
import os
from itertools import count


def formata_tamanho(tamanho_em_bytes: int, base: int = 1000) -> str:
    """Formata um tamanho, de bytes para o tamanho apropriado"""

    # Original:
    # https://stackoverflow.com/questions/5194057/better-way-to-convert-file-sizes-in-python

    # Se o tamanho for menor ou igual a 0, 0B.
    if tamanho_em_bytes <= 0:
        return "0B"

    # Tupla com os tamanhos
    #                      0    1     2     3     4     5
    abreviacao_tamanhos = "B", "KB", "MB", "GB", "TB", "PB"
    # Logaritmo -> https://brasilescola.uol.com.br/matematica/logaritmo.htm
    # math.log vai retornar o logaritmo do tamanho_em_bytes
    # com a base (1000 por padrão), isso deve bater
    # com o nosso índice na abreviação dos tamanhos
    indice_abreviacao_tamanhos = int(math.log(tamanho_em_bytes, base))
    # Por quanto nosso tamanho deve ser dividido para
    # gerar o tamanho correto.
    potencia = base ** indice_abreviacao_tamanhos
    # Nosso tamanho final
    tamanho_final = tamanho_em_bytes / potencia
    # A abreviação que queremos
    abreviacao_tamanho = abreviacao_tamanhos[indice_abreviacao_tamanhos]
    return f'{tamanho_final:.2f} {abreviacao_tamanho}'


caminho = os.path.join(r'c:\\Users\\', 'luizh', 'Pictures')
counter = count()

for root, dirs, files in os.walk(caminho):
    the_counter = next(counter)
    print(the_counter, 'Pasta atual: ', root)

    for dir_ in dirs:
        print('  ', the_counter, 'Dir: ', dir_)

    for file_ in files:
        caminho_completo_arquivo = os.path.join(root, file_)

        stats = os.stat(caminho_completo_arquivo)
        tamanho = stats.st_size

        print('  ', the_counter, 'Dir: ', file_, formata_tamanho(tamanho))

```
- Seguindo o código anterior, bascicamente pegamos o tamanho do arquivo, com "os.stat", que nos retornou um "stat result object" e dele pegamos o tamanho do arquivo.
- Só adicionar ele no print, com uma função pronta do stackoverflow que converte bites em tamanhos convencionais (kb, mb, gb).

# Veja também
- [[Copiando arquivos de um diretório para outro (um por um)]]
- [[Copiando arquivos de um diretório para outro (direto)]]

# Reference
- [Curso de Python do Luiz Otávio Miranda](https://www.udemy.com/user/luiz-otavio-miranda)
- https://docs.python.org/3/library/os.html
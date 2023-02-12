tags: #programação/python 
Doc: https://docs.python.org/3/library/pathlib.html

# Por que usar a pathlib?
- Geralmente, usada para trabalhar com caminhos em um sistema operacional.

# Obtendo caminho do projeto
```Python
caminho_projeto = Path()
print(caminho_projeto.absolute())
```
- Primeiramente, instanciamos a classe path, que retornará o **caminho relativo**, mas queremos o **caminho absoluto**, então utilizamos o método "absolute".

# Obtendo o caminho do arquivo atual
```Python
caminho_arquivo = Path(__file__)
print(caminho_arquivo)
```
- O python já tem uma variável que retorna o caminho completo, então, basta passar  ela por parâmetro.

# Obtendo o caminho da pasta acima
```Python
caminho_arquivo = Path(__file__)
print(caminho_arquivo.parent)
```
- Basta usar o método "parent". Você pode ir subindo as pastas, passando mais um parent, através de "chain responsibility".

# Criando pastas e arquivos
```Python
caminho_arquivo = Path(__file__)
print(caminho_arquivo.parent / 'ideias')
```
- A pathlib utiliza o `__truediv__` para concatenar caminhos. Então para criar um caminho novo, basta passar algum caminho, parent do meu caminho principal por exemplo, e o nome do arquivo que deseja criar O CAMINHO.

# Obtendo a home
- Simplesmente faça: `Path.home()`.

# Salvando e apagando arquivo
```Python
arquivo = Path.home() / 'Desktop' / 'arquivo.txt'
arquivo.touch()
```
- Apenas criamos o caminho, e oficializamos ele usando o método "touch".

```Python
arquivo = Path.home() / 'Desktop' / 'arquivo.txt'
arquivo.unlink()
```
- Isso mesmo...

# Escrevendo dados dentro de um arquivo
## Básico
```Python
arquivo: Path = Path.home() / 'Desktop' / 'arquivo.txt'
arquivo.touch()
arquivo.write_text('Olá mundo!')
```
- Auto descritivo.

```Python
arquivo: Path = Path.home() / 'Desktop' / 'arquivo.txt'
arquivo.touch()
arquivo.write_text('Olá mundo!')
print(arquivo.read_text()) 
```
- Printei o que estava dentro do arquivo.

## Avançado
```Python
caminho_arquivo: Path = Path.home() / 'Desktop' / 'arquivo.txt'
with caminho_arquivo.open('a+') as file:
    file.write('Uma linha\n')
    file.write('Outra linha\n')
```
- Basta utilizar o context manager padrão.

# Criando pastas 
```Python
caminho_pasta: Path = Path.home() / 'Desktop' / 'Pasta_deletar'
caminho_pasta.mkdir()
```
- Se quiser ignorar a exeção que o arquivo já existe, passa-se o parâmetro "exist_ok=True".

# Apagando pastas de forma recursiva
- Tem maneiras mais fáceis de fazer isso, utilizando o módulo "shutil" citado em ([[Copiando arquivos de um diretório para outro (direto)]]).

```Python
def rmtree(root: Path, remove_root=True):
    for file in root.glob('*'):
        if file.is_dir():
            rmtree(file, False)
            file.rmdir()
        else:
            file.unlink()

    if remove_root:
        root.rmdir()
```
- Isto é um função recursiva ([[Funções recursivas]]) que, remove as pastas e arquivos recursivamente. 

# Reference
- https://www.youtube.com/watch?v=T17BTNKBeJY
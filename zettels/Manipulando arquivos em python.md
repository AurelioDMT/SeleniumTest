tags: #programação/python 
status: #zettel/fleeting

# Context manager
- Basicamente, o context manager do python, abre o arquivo (utilizando a [[função open em python]]) e fecha, podendo executar tudo dentro do bloco "with" sem se preocupar em fechar o arquivo.
```Python
with open(carminho_arquivo, 'w', encoding='utf8') as arquivo:
    print('arquivo fechado.')
```
- Nesse código acabamos de instanciar "arquivo". Como dito na função open, retorna um file object, da classe TextIOWrapper.
- Utilizei o parâmetro nomeado "encoding", para escrever em utf-8, já que o windows não escreve.

## Métodos úteis do TextIOWrapper
| Funções | Descrição |
| - | - |
| write() | Escreve.
| read() | Lê.
| writelines() | Escreve várias linhas.
| readlines() | Lê várias linhas.
| seek() | Move o cursor.

# References
- [Curso de Python do Luiz Otávio Miranda](https://www.udemy.com/user/luiz-otavio-miranda)

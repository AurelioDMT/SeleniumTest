tags: #programação/python 
status: #zettel/fleeting

# Como definir uma função
- Em python, definimos uma função com a palavra privada "def".
```Python
def soma(a, b):
	return a + b

def soma()
	print(1 + 1)
```

# Para que serve uma função
- Geralmente uma função, serve para criar um bloco de código para utilizar uma ou várias vezes durante o código.

# Como funciona uma função
- Um função pode ou não, receber parâmetros. E uma função pode ou não, retornar algo.

## Parâmetros e argumentos
- Na definição, ou seja, na criação da função. Você coloca os **parâmetros**.
- Ex: `def soma(parâmetro_1, parâmetro_2)`.

- Quando essa função for chamada, ai, você passa os **argumentos**.
- Ex: `soma(argumento_1, argumento_2)`.

## Parâmetros e argumentos nomeados
- Na definição, você pode usar parâmetros nomeados para definir um valor fixo para os **parâmetros**.
- Ex: `def soma(param_1=0, param_2=None)`.
	- Você também pode passar "None" de **parâmetro**, isso permite a opção de passar ou não o **argumento**.

- Você também pode passar **argumentos** nomeados, mas depois que passa o primeiro, os próximos terão de ser obrigatoriamente nomeados.
- Ex: `soma(param_2=20, param_1=10).

## Função como referência e executada
- Eu posso referenciar uma função:
```Python
def soma(x, y):
	return x + y


print(soma)
--------------------------------------------------------
<function soma at 0x000001AEBFCE3E20>
```

- Como, posso executa-la:
```Python
def soma(x, y):
	return x + y


print(soma(2, 3))
--------------------------------------------------------
5
```

## Args
- `*args`, é um **parâmetro** não nomeado, que desempacota qualquer valor recebido, responsável por receber vários valores e empacotar em uma tupla.

### Exemplo: função que soma todos os argumentos passados
```Python
def soma(*args):
	total = 0
	for numero in args:
		total += numero

	return total
```

## kwargs
- É basicamente igual ao args, só que envez de uma tupla, é um dicionário. Com **parâmetros** nomeados.

### Exemplo de código args e kwargs
```Python
def mostrar_argumentos_nomeados(*args, **kwargs):
    print('NÃO NOMEADOS:', args)

    print()
    print('NOMEADOS:')
    for chave, valor in kwargs.items():
        print(f'Chave: {chave}, Valor: {valor}')


arg_nomeado = {
    "arg1": 1,
    "arg2": 2,
    "arg3": 3,
    "arg4": 4,
}
arg_nao_nomeado = (1, 2, 3, 4)

mostrar_argumentos_nomeados(*arg_nao_nomeado, **arg_nomeado)
-----------------------------------------------------------------
NÃO NOMEADOS: (1, 2, 3, 4)

NOMEADOS:
Chave: arg1, Valor: 1
Chave: arg2, Valor: 2
Chave: arg3, Valor: 3
Chave: arg4, Valor: 4
```
- Nesse código, usamos um asterisco para desempacotar uma tupla, e dois asteriscos para desempacotar um dicionário.

### Exemplo de parâmetros nomeados
```Python
def mostrar_argumentos_nomeados(*args, **kwargs):
    for k, v in kwargs.items():
        print(k, v)


mostrar_argumentos_nomeados(
    nome='Luiz',
    sobrenome='Henrique',
    idade=21,
)
```

## Função lambda
- A função lambda é como qualquer outra função em python, o diferencial dela é, você pode escrever ela em somente uma linha.

### Exemplo de uso da função lambda
```Python
lista = [
	{'nome': 'Luiz', 'sobrenome': 'miranda'},
	{'nome': 'Maria', 'sobrenome': 'Oliveira'},
	{'nome': 'Daniel', 'sobrenome': 'Silva'},
	{'nome': 'Eduardo', 'sobrenome': 'Moreira'},
	{'nome': 'Aline', 'sobrenome': 'Souza'},
]

def exibir(lista):
	for item in lista:
		print(item)
	print()


l1 = sorted(lista, key=lambda item: item['nome'])
l2 = sorted(lista, key=lambda item: item['sobrenome'])

exibir(l1)
exibir(l2)
--------------------------------------------------------------
{'nome': 'Aline', 'sobrenome': 'Souza'}
{'nome': 'Daniel', 'sobrenome': 'Silva'}
{'nome': 'Eduardo', 'sobrenome': 'Moreira'}
{'nome': 'Luiz', 'sobrenome': 'miranda'}
{'nome': 'Maria', 'sobrenome': 'Oliveira'}

{'nome': 'Eduardo', 'sobrenome': 'Moreira'}
{'nome': 'Maria', 'sobrenome': 'Oliveira'}
{'nome': 'Daniel', 'sobrenome': 'Silva'}
{'nome': 'Aline', 'sobrenome': 'Souza'}
{'nome': 'Luiz', 'sobrenome': 'miranda'}
```

## Escopo de função
- Basicamente, todas as varíaveis que você declarar em um função, pertence somente a ela mesma.

- A não ser que você use a palavra privada "global" antes da variável, ai uma função é capaz de modificar outra variável de fora dela.

## Call stack
- Quando um código está executando, e chamamos uma função. O código principal suspende na memória, para que a função seja executada em outra parte da memória. Sendo assim literalmente uma pilha, sendo que quando terminado o processo, retornará ao código principal.

- Você pode observar tudo isso debugando ([[Debug]]).

# References
- https://www.udemy.com/course/python-3-do-zero-ao-avancado/learn/lecture/34638344#overview (Cap 4. ep. 105)

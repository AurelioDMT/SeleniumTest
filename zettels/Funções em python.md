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
- `*args`, é um **parâmetro** que desempacota qualquer valor recebido, responsável por receber vários valores e empacotar em uma tupla.

### Exemplo: função que soma todos os argumentos passados
```Python
def soma(*args):
	total = 0
	for numero in args:
		total += numero

	return total
```


## Escopo de função
- Basicamente, todas as varíaveis que você declarar em um função, pertence somente a ela mesma.

- A não ser que você use a palavra privada "global" antes da variável, ai uma função é capaz de modificar outra variável de fora dela.

## Call stack
- Quando um código está executando, e chamamos uma função. O código principal suspende na memória, para que a função seja executada em outra parte da memória. Sendo assim literalmente uma pilha, sendo que quando terminado o processo, retornará ao código principal.

- Você pode observar tudo isso debugando ([[Debug]]).

# References
- https://www.udemy.com/course/python-3-do-zero-ao-avancado/learn/lecture/34638344#overview (Cap 4. ep. 105)

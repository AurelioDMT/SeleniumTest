tags: #programação/python  
status: #zettel/fleeting

# Sintaxe
```Python
var = [x for x in range(10)
-------------------------------
[0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
```
- O "x" antes do for, é o que vai ser incluido na lista, depois segue a sintaxe normal de um "for".

- Esse código faz a mesma coisa que esse:
```Python
lista = list()
for numero in range(10):
    lista.append(numero)
```
---
- ==Você pode utilizar o "if", à esquerda do for, como mapeamento e, à direita do for, como filtro==.
- O "if" antes do for, necessariamente precisa ter o "else". O "if" depois do for não terá "else".
```Python
var = ['hey' if x == 6 else x for x in range(10) if x % 2 == 0]
------------------------------------------------------------------
[0, 2, 4, 'hey', 8]
```
---
- Utilizando 2 "for's":
```Python
lista = [(x, y) for x in range(3) for y in range(3)]
```

- Que faz a mesma coisa que esse:
```Python
lista = list()
for x in range(3):
    for y in range(3):
        lista.append((x, y))
```
---
- List comprehension dentro de list comprehension
```Python
lista = [
    [x for y in range(3)]
    for x in range(3)
]
----------------------------------
[[0, 0, 0], [1, 1, 1], [2, 2, 2]]
```
- Nesse caso, pra cada volta do for, eu vou fazer outra lista com o for interior.

# Mapeamento
- Mapeamento, nada mais é do que você somente trocar os valores de uma lista. Logo, o tamanho da lista sempre será o mesmo, permanecendo os indices.

- É feito antes do for

## Exemplo de mapeamento
```Python
produtos = [
    {'nome': 'p1', 'preco': 20},
    {'nome': 'p2', 'preco': 10},
    {'nome': 'p3', 'preco': 30},
]

adicionar_5_porcento_se_maior_que_vinte = [
    {**produto, 'preco': produto['preco'] * 1.05}
    if produto['preco'] > 20 else {**produto}
    for produto in produtos
]
------------------------------------------------------
{'nome': 'p1', 'preco': 20}
{'nome': 'p2', 'preco': 10}
{'nome': 'p3', 'preco': 34.5}
```

# Filtro
- Filtro controla se você inclui ou não um elemento.

- É feito depois do for

## Exemplo de filtro:
```Python
produtos = [
    {'nome': 'p1', 'preco': 20},
    {'nome': 'p2', 'preco': 10},
    {'nome': 'p3', 'preco': 30},
]

adicionar_5_porcento_se_maior_que_vinte = [
    {**produto, 'preco': produto['preco'] * 1.05}
    if produto['preco'] > 20 else {**produto}
    for produto in produtos
    if (produto['preco'] >= 20 and produto['preco'] * 1.05) > 10
]
----------------------------------------------------------------------
{'nome': 'p1', 'preco': 20}
{'nome': 'p3', 'preco': 31.5}
```

# Ver também
- Dict e set comprehension
- Proximo ([[Iteráveis e iteradores em python]])
# References
- [Curso de Python do Luiz Otávio Miranda](https://www.udemy.com/user/luiz-otavio-miranda)

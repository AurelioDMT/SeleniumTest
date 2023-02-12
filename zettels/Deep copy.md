tags: #programação/python 
status: #zettel/fleeting

- Para fazer um **deep copy** (cópia profunda), que copia até os valores imutáveis, precisamos importar um módulo chamado "copy".
```python
import copy
```
- Depois é só utilizar a função *deepcopy()*.
```python
dicionário_1 = {
    'chave_1': 1,
    'chave_2': 2,
    'chave_3': [22, 1]
}

dicionário_2 = copy.deepcopy(dicionário_1)

dicionário_1['chave_3'][0] = 1000

>>> dicionário_1: {'chave_1': 1, 'chave_2': 2, 'chave_3': [1000, 1]}
>>> dicionário_2: {'chave_1': 1, 'chave_2': 2, 'chave_3': [22, 1]}
```
- Perceba que copiou de verdade.

# Alguns exemplos
```Python
from copy import deepcopy
# copy, sorted, produtos.sort
# Exercícios
# Aumente os preços dos produtos a seguir em 10%
# Gere novos_produtos por deep copy (cópia profunda)
produtos = [
    {'nome': 'Produto 5', 'preco': 10.00},
    {'nome': 'Produto 1', 'preco': 22.32},
    {'nome': 'Produto 3', 'preco': 10.11},
    {'nome': 'Produto 2', 'preco': 105.87},
    {'nome': 'Produto 4', 'preco': 69.90},
]

novos_produtos = [
    {**produto, 'preco': produto['preco'] * 1.10}
    for produto in deepcopy(produtos)
]

# Ordene os produtos por nome decrescente (do maior para menor)
# Gere produtos_ordenados_por_nome por deep copy (cópia profunda)

produtos_ordenados_por_nome = sorted(
    deepcopy(novos_produtos), 
    key=lambda item: item['nome'],
    reverse=True
)

# Ordene os produtos por preco crescente (do menor para maior)
# Gere produtos_ordenados_por_preco por deep copy (cópia profunda)

produtos_ordenados_por_preco = deepcopy(produtos_ordenados_por_nome)
produtos_ordenados_por_preco.sort(key=lambda item: item['preco'])
```

# References
- [Curso de Python do Luiz Otávio Miranda](https://www.udemy.com/user/luiz-otavio-miranda)
	- Sec. 4 ep. 121.

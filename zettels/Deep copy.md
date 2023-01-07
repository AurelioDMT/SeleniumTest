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

# References
- [Curso de Python do Luiz Otávio Miranda](https://www.udemy.com/user/luiz-otavio-miranda)
	- Sec. 4 ep. 121.

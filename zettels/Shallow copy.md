tags: #programação/python 
status: #zettel/fleeting

- Se eu der um *copy()* em um dicionário, tudo que for mutável vai para o outro sem problema.
```python
dicionário_1 = {
    'chave_1': 1,
    'chave_2': 2
}

dicionário_2 = dicionário_1.copy()

dicionário_1['chave_1'] = 1000

>>> dicionário_1: {'chave_1': 1000, 'chave_2': 2}
>>> dicionário_2: {'chave_1': 1, 'chave_2': 2}
```
- O problema é quando o dicionário tem um imutável, se tivesse uma lista ou algo assim, se usar o método *copy()*, ele não fazerá a copia. Ele vai fazer que os dois dicionários apontem pra mesma lista na memória.
- Então, por isso **shallow copy** (cópia raza), porque ele não desce em subníveis. 
- Veja como copiar tudo em um dicionário em [[Deep copy]].

# References
- [Curso de Python do Luiz Otávio Miranda](https://www.udemy.com/user/luiz-otavio-miranda)
	- Sec. 4 ep. 121.
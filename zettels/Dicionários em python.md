tags: #programação/python
status: #zettel/fleeting

- Dicionários em Python (tipo dict)
- Dicionários são estruturas de dados do tipo
- par de "chave" e "valor".
- Chaves podem ser consideradas como o "índice"
- que vimos na lista e podem ser de tipos imutáveis
- como: str, int, float, bool, tuple, etc.
- O valor pode ser de qualquer tipo, incluindo outro dicionário.
- Usamos as chaves - {} - ou a classe dict para criar dicionários.
- Imutáveis: str, int, float, bool, tuple
- Mutável: dict, list

```python
pessoa = {
	'nome': 'Luiz Henrique',
	'sobrenome': 'Diogo',
	'idade': 18,
	'altura': 1.8,
	'endereços': [
		{'rua': 'tal tal', 'número': 123},
		{'rua': 'outra rua', 'número': 321},
	],
}
```
---
<center><b>Métodos no dicionário</b></center>

| Metodos | Descrição |
|:--:|:--:|
| *len()* | Mostra quantas chaves o dicionário tem. |
| *keys()* | Retorna um iterável dict_keys object com as chaves. |
| *values()* | Retorna um iterável dict_values object com o valor. |
| *items()* | Retorna um iterável dict_items com valor e chave.|
| *setdefault()* | Adiciona valor se a chave não existe. |
| *copy()* | Retorna uma cópia rasa ([[Shallow copy]]) |
| *get()* | Obtém uma chave. |
| *pop()* | Apaga um item com a chave específica. |
| *popitem()* | Apaga o útimo item adicionado. |
| *update()* | Atualiza um dicionário com outro. |
| *clear()* | Remove todos os elementos de um dicionário. |
| *fromkeys()* | Retorna um dicionário com as chaves e valores especificados. |

# References
- [Curso de Python do Luiz Otávio Miranda](https://www.udemy.com/user/luiz-otavio-miranda)
	- Sec. 4 ep. 118 - 122.
- [Site da w3schools](https://www.w3schools.com/python/python_ref_dictionary.asp)
	- Python Dictionary Methods
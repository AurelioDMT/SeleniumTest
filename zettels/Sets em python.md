tags: #programação/python
status: #zettel/fleeting

- Sets em Python (tipo set).
- É um iterável.
- Sets paracem dicionários, só que sem a parte do "chave" e "valor".
- Aceita somente tipos imutáveis em seu interior, porém é mutável.
- Usamos também as chaves, mas nunca vazia, se não, vira dicionário - {} - ou a classe set para criar sets.

```Python
set = {1, 2, 3, 4}

set_1 = set('Luiz')
print(set_1)
-------------------------------------------------------------
{'u', 'L', 'i', 'z'}
```

# Pra que serve o set
- Seus valores sempre serão únicos.
- Não aceitam valores mutáveis
- Não tem índices.
- Não garantem ordem.
---
<center><b>Métodos no set</b></center>
| Métodos | Descrição |
| :-: | :-: |
| add() | Adiciona um elemento no set. |
| clear() | Remove todos os elementos de um set.
| copy() | Retorna uma cópia do set.
| difference() | Retorna outro set, contendo a diferença entre dois ou mais sets.
| difference_update() | Remove os item do conjunto que também estão incluído no outro.
| discard() | Remove um item específico.
| intersection() | Retorna um set que é a interseção de dois ou mais sets.
| intersection_update() | Remove os items em um set, que não estão presentes no outro.
| isdisjoint() | Retorna se dois sets tem interseção ou não.
| issubset() | Retorna se outro set contém esse set ou não.
| issuperset() | Retorna se esse set contém outro set ou não.
| pop() | Remove um elemento do set.
| remove() | Remove um elemento específico.
| symmetric_difference() | Retorna um set que é a diferença simétrica entre sets.
| symmetric_difference_update() | Insete a diferença simétrica desse set para outro.
| union() | Retorna um set contendo a união de sets.
| update() | Atualiza o set com outro, ou qualquer iterável.

# References
- [Curso de Python do Luiz Otávio Miranda](https://www.udemy.com/user/luiz-otavio-miranda)
- https://www.w3schools.com/python/python_ref_set.asp
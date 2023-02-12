tags: #programação/python 

- Esse é um exercicio do curso de python.

```
# Exercício - Unir listas
# Crie uma função zipper (como o zipper de roupas)
# O trabalho dessa função será unir duas
# listas na ordem.
# Use todos os valores da menor lista.
# Ex.:
# ['Salvador', 'Ubatuba', 'Belo Horizonte']
# ['BA', 'SP', 'MG', 'RJ']
# Resultado
# [('Salvador', 'BA'), ('Ubatuba', 'SP'), ('Belo Horizonte', 'MG')]
```

# Minha  resposta
```Python
def zipper(l1, l2):
    menor = l1
    maior = l2
    if len(l2) < len(l1):
        menor = l2
        maior = l1

    lista_final = list()
    for y, x in enumerate(menor):
        valor = menor[y], maior[y]
        lista_final.append(valor)
    
    return lista_final
```

# Resposta do professor
```Python
def zipper(l1, l2):
    intervalo = min(len(l1), len(l2))
    return [(l1[i], l2[i]) for i in range(intervalo)]
```
- Perceba que ele foi direto ao ponto, pegou o tamanho da menor lista e usou como indice no range.

# Porém
- Essa função ja existe no python, `zip()`.
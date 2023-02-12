tags: #programação/python/funções  

# Definição e uso
- A função "map()" executa uma função expecífica para cada item em um iterável ([[Iteráveis e iteradores em python]]). O item é enviado para função como parâmetro ([[Funções em python]]).

- Retorna um map object, que é um iterável.

# Sintaxe
- `map(function, iterables)`

## Valor dos parâmetros
| Parâmetro | Descrição |
| - | - |
| function | Requerida. A função que é executada para cada item.
| iterable | Requerida. Uma sequência, coleção ou um objeto iterador.
| iterable* | Opcional. Pode mandar quantos iteráveis quiser, certifique-se que a função tem um parâmetro pra cada iterável.

# Exemplos
```Python
from functools import partial

produtos = [
    {'nome': 'Produto 5', 'preco': 10.00},
    {'nome': 'Produto 1', 'preco': 22.32},
    {'nome': 'Produto 3', 'preco': 10.11},
    {'nome': 'Produto 2', 'preco': 105.87},
    {'nome': 'Produto 4', 'preco': 69.90},
]


def aumentar_porcentagem(valor, porcentagem):
    return round(valor * porcentagem, 2)


aumentar_dez_porcento = partial(
    aumentar_porcentagem,
    porcentagem=1.1
)

def muda_preco_de_produtos(produto):
    return {
        **produto,
        'preco': aumentar_dez_porcento(
            produto['preco']
        )
    }


novos_produtos = map(
    muda_preco_de_produtos,
    produtos
)

print(novos_produtos)
```

# Reference
- https://www.w3schools.com/python/ref_func_map.asp
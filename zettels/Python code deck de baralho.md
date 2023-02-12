tags: #programação/python/code 

# Composição
- Descrição: é o primeiro código citado no livro "Python fluente", basicamente gera um objeto iterável com as cartas de baralho.
```Python
import collections


Card = collections.namedtuple('Card', ['numero', 'naipe'])

class FrenchDeck:
    ranks = [str(n) for n in range(2, 11)] + list('JQKA')
    naipe = 'espadas ouro paus copas'.split()

    def __init__(self):
        self._cards = [Card(rank, naipe) for naipe in self.naipe
                                        for rank in self.ranks]
    def __len__(self):
        return len(self._cards)

    def __getitem__ (self, position):
        return self._cards[position]
```
---
- Como um baralho funciona: [[Baralho]].

- A primeira atribuição: `Card = collections.namedtuple('Card', ['numero', 'naipe'])`
- Me gera uma **named tuple**, que é um objeto "Card", que exibe os 2 parâmetros "numero" e "naipe".
	- Card(numero='2', naipe='♠')

- Dentro da classe "FrenchDeck", há duas lógicas para atribuir todos os valores de número e naipe.
	- **Primeira lógica** (numeros): `ranks = [str(n) for n in range(2, 11)] + list('JQKA')`
	- Retorna uma lista que é feita de strings que, pra cada numero em um range do indice 2 até 11, ou seja, ==números de 2 até 10==, e concatenando com outra lista com os valores `['J', 'Q', 'K', 'A']`.
	- Retorno: `['2', '3', '4', '5', '6', '7', '8', '9', '10', 'J', 'Q', 'K', 'A']`

	- **Segunda lógica** (naipes): `naipe = 'espadas ouro paus copas'.split()`
	- Basicamente retorna uma lista para cada palavra digitada.

- No método "`__init__`", `self._cards_` é atribuido como atributo priavado.
- Recebe uma lista. Como dito antes, o objeto **named tuple**, só está como um molde, essa lista retorna exatamente esse objeto preenchido com todas as cartas de um baralho. Ou seja 52 cartas, 4 grupos (naipes) e cada grupo com 13 cartas.
	- Último indice: `51, Card(numero='A', naipe='♥')`

- No método "`__len__`", somente seta o len do objeto para o len das cartas, que no caso é 52.

- No método "`__getitem__`", ele transforama a classe "FrenchDeck" em um iterável, que no caso é uma lista.

# Conteúdo usado
- [[List comprehension em python]]
- [[POO em python (programação orientada a objeto)]]
- [[Iteráveis e iteradores em python]]
- [[Baralho]]

# Reference
- Livro: Python fluente
tags: #estudos/matemática 

# Introdução
1. Na teoria dos conjuntos três noções são aceitas sem definição:
	- a) conjunto;
	- b) elemento;
	- c) pertinência entre elemento e conjunto.

- É possível expressar os conjuntos de duas maneiras: através de chaves e através de diagrama (embaixo):
	- ![[Pasted image 20230401051602.png]]

- Seguindo o conjunto acima, uma pertinência é a representação se o número pertence "$\in$" e se não pertence "$\notin$".
$$Pertinência \begin{cases}1 \in a \\5 \notin b \end{cases}$$

2. Descrição de um conjunto
	- a) Descrição pela citação de elementos
		- Conjutno das vogais
			- V = {a, e, i, o, u}
		- Conjunto dos estados que fazem parte da região sul do Brasil
			- E = {PR, SC, RS}
		- Conjunto dos números primos positivos
			- P = {2, 3, 5, 7, 11, 13, ...}
		- Conjuntos dos números inteiros de 0 a 300
			- I = {0, 1, 2, ..., 298, 299, 300}
	- b) Descrição por uma propriedade
		- A = {x | x tem a propriedade P}
			- | = tal que.
			- A = {x | x é divisor inteiro de 5}
			- Logo, A = {-1, -5, 1, 5}
			- B = {x $\in \mathbb{N}$ | x < 3}
			- Logo, B = {0, 1, 2}

3. Conjunto unitário
	- Possui um único elemento.
	- C = {x $\in \mathbb{N}$ | 3 < x < 5}
	- Logo, C = {4}

4. Conjunto vazio
	- Não possui elemento algum. 
	- V = {x | x é impar e divisível por 2}
	- V = {} ou $\varnothing$

5. Conjunto universo
	- Quando desenvolvemos um assunto em matemática, admitimos a existência de um conjunto U ao qual pertencem todos os elementos utilizados nesse assunto. Esse conjunto U é chamado de conjunto universo.

6. Conjuntos iguais
	- Dois conjuntos são iguais quando possuem os mesmos elementos.
	- A = {a, b, c}
	- B = {c, b, a}
	- Logo, A = B
	- C = {1, 2}
	- D = {1, 2, 2, 2}
	- Logo, C = D

7. Subconjuntos
	- Um conjunto A é subconjunto de um conjunto B se todo elemento de A é também elemento de B
	- A = {a, b}
	- B = {a, b ,c}
	- Logo, A $\subset$ B
		- $\subset$ = está contido
		- logo, A está contido em b; ou
		- A é subconjunto de B; ou
		- A é parte de B.
	- C = {2, 3, 4}
	- D = {4, 5}
	- Logo, C $\not\subset$ D
	- E = {1, 2}
	- F = {3}
	- Logo, E e F são conjuntos disjuntos!
	- G = {1, 2}
	- H = {1, 2}
	- Logo, G $\subset$ H e H $\subset$ G

8. Propriedades da inclusão
	- P1) $\varnothing$ $\subset$ A
	- P2) A $\subset$ A
	- P3) A $\subset$ B = B $\supset$ A

9. Conjunto das partes
	- Seja um conjunto A, o conjunto das partes de A, representado por P(A), é o conjunto formado por todos os subconjuntos de A
	- A = {1, 2} $\overset{subconjuntos}{\rightarrow}$ {1}, {2}, {1, 2}, $\varnothing$
	- Logo, P(A) = {{1}, {2}, {1, 2}, $\varnothing$}
	- Nº de subconjuntos:
		- Se A possui n elementos, então o nº de subconjuntos de  A é $A^n$
	- Então o número de elementos de A é 2. Logo 2² = 4 subconjuntos

# União ou Reunião
1. Dados dois conjuntos A e B, chama-se **união** de A e B o conjunto formado pelos elementos que pertencem a A ou a B
	- A U B = {x | x $\in$ A ou x $\in$ B}
	- Exemplos:
		- a) A = {a, b ,c} e B = {c, d}
		- A U B = {a, b, c, d}
		- b) A = {5, 6} e B = {8, 9}
		- A U B = {5, 6, 8, 9}
		- c) A = {4, 7} e B = {4, 6, 7}
		- A U B = {4, 6, 7}

2. Propriedades da União
	- P1) A U A = A
	- P2) Elemento Neutro da União
		- A U $\varnothing$ = A
	- P3) Comutativa
		- A U B = B U A
	- P4) Associativa
		- (A U B) U C = A U (B U C)

# Intersecção
1. Dados dois conjuntos A e B, chama-se **intersecção** de A e B o conjunto formado pelos elementos que pertencem a A e a B
	- A $\cap$ B = {x | x $\in$ A e x $\in$ B}
	- Exemplos:
		- a) A = {a, b, c} e B = {c, d}
		- A $\cap$ B = {c}
		- b) A = {5, 6} e B = {8, 9}
		- A $\cap$ B = $\varnothing$
		- c) A = {4, 7} e B = {4, 6, 7}
		- A $\cap$ B = {4, 7}

2. Propriedades da intersecção
	- P1) A $\cap$ A = A
	- P2) Elemento neutro da intersecção
		- A $\cap$ U = A
	- P3) Comutativa
		- A $\cap$ B = B $\cap$ A
	- P4) Associativa
		- (A $\cap$ B) $\cap$ C = A $\cap$ (B $\cap$ C)
	- Número de elementos da União
		- Exemplo:
			- A = {1, 3, 5, 7, 9}
			- B = {2, 3, 5, 7}
			- n(A U B) = n(A) + n(B) - n(A $\cap$ B)
			- 6 = 5 + 4 - 3
			- 6 = 6
		- Exemplo:
			- A = {a, b, c}
			- B = {d, e}
			- n(A U B) = n(A) + n(B) pois A e B são disjuntos.
			- 5 = 3 + 2
		- Exemplo:
			- ![[Pasted image 20230403092350.png]]

# Diferença de conjuntos
1. Dados dois conjuntos A e B, chama-se **diferença** entre A e B o conjunto formado pelos elementos de A que não pertencem a B
	- A - B = {x | x $\in$ A e x $\not\in$ B}
	- Exemplos:
		- a) A = {1, 2, 3, 4} e B = {2, 4, 5}
		- A - B = {1, 3}
		- B - A = {5}
		- b) A = {a, b, c} e B = {d, e}
		- A - B = A
		- B - A = B poque A e B são disjuntos!
		- c) A = {a, b} e B = {a, b, c}
		- A - B = {}
		- B - A = {c}

# Complementar de B em A
1. Dados dois conjuntos A e B, tais que B $\subset$ A, chama-se **complementar de B em relação a A** o conjunto A - B
	- $\complement_{A}^B$ = A - B (B $\subset$ A)
	- Exemplos:
		- A = {0, 2, 4, 6, 8}
		- B = {0, 4, 8}
		- $\complement_{A}^B$ = A - B = {2, 6}

# Reference
- https://youtu.be/0aUEDxYjZg8?list=PLTPg64KdGgYgTXWPsURDnPBd7GUwPVBLx
- https://youtu.be/Wxm3ugnq9Sw?list=PLTPg64KdGgYgTXWPsURDnPBd7GUwPVBLx
- https://youtu.be/c5a99sX-Sq8?list=PLTPg64KdGgYgTXWPsURDnPBd7GUwPVBLx
- https://youtu.be/eZfFpnvudR0?list=PLTPg64KdGgYgTXWPsURDnPBd7GUwPVBLx

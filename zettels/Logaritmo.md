tags: #estudos/matemática 

# Definição:
- Logaritmo é uma ==função matemática== que está ==baseada nas propriedades da potenciação e exponenciação==. O valor do logaritmo corresponde ao expoente que se deve elevar uma determinada base, positiva e diferente de 1, para que o resultado seja igual a um número positivo b.
$$\log_{a}{b} = x <=> a^{x} = b$$
- Fala-se: Logaritmo de a na base b, sendo a > 0 e a ≠ 1 e b > 0.
---
$$a^{\log_{a}{b}} = b$$
- Desta forma, o logaritmo é a uma operação na qual queremos descobrir o expoente que uma dada base deve ter para resultar em uma certa potência.

Ex:
- $\log_{6}{36} = 2$, pois $6^2 = 36$
- $\log_{2}{16} = 4$, pois $2^4 = 16$
- $\log_{\frac{1}{5}}{5} = -1$, pois $(\frac{1}{5})^{-1} = 5$

# Propriedades 
1. Quando o logaritmando é igual à base, o logaritmo será sempre igual a 1.
$$\log_{a}{a} = 1$$
2. Logaritmo de qualquer base, cujo logaritmando seja igual a 1, terá sempre o resultado igual a 0.
$$\log_{a}{1} = 0$$
3. Quando um logaritmo possui a base igual a 10, esse é chamado logaritmo decimal. Ao registrar-se um logaritmo decimal, não é necessário escrever a base 10. É convencionado que:
$$\log_{10}{b} = \log{b}$$
4.  Quando a base for igual ao logaritimando e o logaritimando for uma exponenciação, o resultado é igual ao expoente.
$$\log_{a}{a^m} = m$$
5. Dois logaritmos com a mesma base são iguais quando os logaritmandos também são iguais.
$$\log_{a}{b} = \log_{a}{c} => b = c$$
6. Uma potência de base **a** e expoente igual a logaritmo de **b** na base **a**, é igual a **b**.
$$a^{\log_{a}{b}} = b$$
7. Quando o logaritmando é composto por uma multiplicação de números, podemos separá-los numa soma de logaritmos com a mesma base para ambos.
$$\log_{a}{MN} = \log_{a}{M} + \log_{a}{N}$$
8. Quando o logaritmando é composto por uma divisão de números, podemos separá-los numa subtração de logaritmos, com a mesma base para ambos.
$$\log_{a}{(\frac{M}{N})} = \log_{a}{M} - \log_{a}{N}$$
9. A regra da potência: o logaritmo de uma potência simplifica-se multiplicando o expoente pelo logaritmo, mantendo a mesma base e o logaritmando.
$$\log_{a}{(M^k)} = k\log_{a}{M}$$
10. Para mudar a base de um logaritmo, usamos o seguinte.
$$\log_{b}{c} = \frac{\log_{a}{c}}{\log_{a}{b}}$$
11. O logaritmo de uma raiz é igual ao inverso do índice da raiz multiplicado pelo logaritmo, em que também mantemos a base.
$$\log_{a}{\sqrt[n]{b}} = \frac{1}{n}\log_{a}{b}$$

# Exercicios
## 1. CESGRANRIO - 2022
Um banco montou um índice de desempenho (L) para um de seus serviços. O índice se refere a um atributo numérico, representado por A, sempre positivo. Por conta de o atributo A assumir valores muito altos, o índice L montado pelo setor técnico do banco foi concebido por L = $\log_{10}{(A)}$. Há uma meta de que, nos próximos 5 anos, o índice L aumente em duas unidades. 

A meta, portanto, indica que é esperado que, nos próximos 5 anos, o atributo A seja igual

(A) ao atributo A atual aumentado em 2 unidades.
(B) ao atributo A atual aumentado em 100 unidades.
(C) a 2 vezes o atributo A atual.
(D) a 10 vezes o atributo A atual.
(E) a 100 vezes o atributo A atual

---
$\log_{10}{(A)} = L <=> 10^{L} = A$ 
$\log_{10}{A} = L + 2$
$10^{L + 2} = A$

Uma **exponenciação** com base 10 é sempre uma casa decimal a mais. Ex: $10^4 = 10.000$ (4 zeros).
Logo, se adicionou **2 unidades** ao expoente, multiplicou **100 vezes** do outro lado.

## 2. UFRGS - 2014
Atribuindo para log 2 o valor 0,3, então os valores de log 0,2 e log 20 são, respectivamente,

a) - 0,7 e 3 .  
b) - 0,7 e 1,3.  
c) 0,3 e 1,3.  
d) 0,7 e 2,3.  
e) 0,7 e 3.

---
$\log{(\frac{2}{10})}$
$\log{2} - \log{10} = 0,3 -1 = -0,7$ 

$\log20$
$\log20 = log(10*2)$
$\log20 = \log10 + \log2$
$\log20 = 1 + 0,3 = 1,3$

# Reference
- https://www.significados.com.br/logaritmo/#:~:text=Definição%20de%20logaritmo%3A,a%20um%20número%20positivo%20b
- https://www.todamateria.com.br/logaritmo/
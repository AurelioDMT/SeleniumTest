tags: #estudos/matemática 

- Definição
> Equação do 2º grau, na variável real *x*, é toda equação da forma $ax^2 + bx + c = 0$, no qual *a,b,c* pertencem aos reais, com $a \neq 0$.

- Exemplos
- $3x^2 - 5x + 2 = 0$
	- a=3, b=-5, c=2
	- Esses são os coeficiente de suas respectivas variáveis.
- $\frac{2}{3}x + x^2 = 0$
	- a=1, b=$\frac{2}{3}$, c=0
- $3x^2 - 9 = 0$
	- a=3, b=0, c=-9
	- Se há uma variável igual a 0, que não seja *a*, chama-se de enquação do 2º grau **incompleta**.

# Raiz de uma equação do 2º grau
- Uma equação do segundo grau possui no máximo duas raízes. Essas raízes podem ser determinadas através da seguinte fórmula, que é conhecida como fóruma de Bhaskara:
$$\frac{-b \pm \sqrt{b^2 - 4ac}}{2a}$$
- Exemplos
- $2x^2 - 9x + 7 = 0$
	- a=2, b=-9, c=7
	- $\frac{-(-9) \pm \sqrt{(-9)^2 - 4*2*7}}{2*2}$
	- $\frac{-(-9) \pm \sqrt{25}}{2*2}$
	- $\frac{9 \pm 5}{4}$
	- $x_1 = \frac{9 + 5}{4} = \frac{14}{4} = \frac{7}{2} = 3,5$
	- $x_2 = \frac{9 - 5}{4} = \frac{4}{4} = 1$
	- S = {1, $\frac{7}{2}$}

# Equações incompletas
- Essas equações podem ser mais simples de resolver, podendo optar por não usar **a fórmula de bhaskara**.

- 1º caso: $b = 0$
	- $2x^2 - 24 = 0$
	- $2x^2 = 24$
	- $x^2 = 12$
	- $x = \pm \sqrt{12}$
	- $x = \pm 2\sqrt{3}$
		- $x_1 = 2\sqrt{3}$
		- $x_2 = -2\sqrt{3}$
	- S = {$2\sqrt{3}$, $-2\sqrt{3}$}
- 2º caso: $c = 0$
	- $4x^2 - 6x = 0$
	- $2x(2x - 3) = 0$
	- Na matemática, se 2 número estiverem se multiplicando e forem igual a zero, é certo que um destes números é igual a 0. Logo, 2x = 0 ou 2x - 3 = 0.
	- Então, resolvem-se as opções: $x_1 = 0, x_2 =\frac{3}{2}$ respectivamente.
	- S {0, $\frac{3}{2}$}

# Descriminante $\Delta$
- Sobre o descriminante Δ, que separa a **fórmula de bhaskara** em:
- $\frac{-b \pm \sqrt{\Delta}}{2a}$ e $\Delta = b^2 - 4ac$
- Esse descriminante pode assumir 3 possibilidades:
	- $\Delta > 0$ => a equação possui duas raízes reais e diferentes.
	- $\Delta = 0$ => a equação possui duas raízes reais e iguais.
	- $\Delta < 0$ => a equação não possui raízes reais.

- Exemplos:
- $4x^2 - 4x + 1 = 0$
	- a=4, b=-4, c=1
	- $\Delta = (-4)^2 - 4*4*1$
	- $\Delta = 16 - 16 = 0$
	- $x_1 = x_2$
	- $x = \frac{-b}{2a}$ = $\frac{4}{8}$
	- $x_1 = x_2 = \frac{1}{2}$
	- S: {$\frac{1}{2}$}
- $3x^2 + 2x + 1 = 0$
	- a=3, b=2, c=1
	- $\Delta = 2^2 - 4*3*1$
	- $\Delta = -8$
	- $x_1, x_2$ não pertencem aos números reais
	- S = {}

# Relação entre os coeficientes e as raízes
- A equação do 2º grau possui duas importantes relações entre as raìzes $x_1$ e $x_2$ e os coeficientes *a,b* e *c*. Essas relações são conhecidas como **Soma e Produto** ou, também, **Relações de Girard**.

- Soma:
$$x_1 + x_2 = \frac{-b}{a}$$
- Produto:
$$x_1*x_2 = \frac{c}{a}$$
- Exemplos:
- $x^2 + 3x - 10 = 0$
	- a=1, b=3, c=-10
	- Soma: $(2) + (-5) = -3$
	- Produto: $(2) \times (-5) = -10$ 
	- Logo, é necessário achar 2 números que condizem com a soma e o produto.
	- S = {-5, 2}
- Se $x_1$ e $x_2$ são raízes da equação $3x^2 - 6x + 5 = 0$, determine o valor da expressão $\frac{5}{x_1} + \frac{5}{x_2}$.
	- $\frac{5x_2 + 5x_1}{x_1*x_2}$
	- $\frac{5(x_1 + x_2)}{x_1*x_2}$
	- a=3, b=-6, c=5
	- Soma: $=2$
	- Produto: $=\frac{5}{3}$
	- $\frac{5*2}{5/3} = 10*\frac{3}{5} = 6$

# Determinação da equação do 2º grau
- Se $x_1$ e $x_2$ são raízes de uma equação do 2º grau, então essa equação pode ser escrita como:
![[Pasted image 20230208170955.png]]
$$x^2 - Sx + P = 0$$
![[Pasted image 20230208171310.png]]

- Exemplo:
- Determine a equação do 2º grau que possui {3, -7} como conjunto solução.
	- a=1, b=-S, c=P 
	- b = $-(3-7) => b=4$
	- c = $3*(-7) => c = -21$
	- a=1, b=-4, c=-21
	- $x^2 + 4x - 21 = 0$

# Problemas que envolvem a equação do 2º grau
![[Pasted image 20230208172112.png]]
$\begin{cases}p*a = 374\\a + 5 = p\end{cases}$

$(a+5)a = 374$
$a^2 + 5a - 374 = 0$

a=1, b=5, c=-374
$\Delta = 5^2 - 4*1*(-374)$
$\Delta = 25 + 1496$
$\Delta = 1521$

$a = \frac{-5 \pm \sqrt{1521}}{2*1} = \frac{-5 \pm 39}{2}$
	$a_1 = 17 anos$
	$a_2= -22 anos$

Augusto tem 17 anos, equanto Pedro tem 22 anos.

---
![[Pasted image 20230208202649.png]]

d: distância/hora
x: número de dias

$d*x = 240$
$(d+4)(x-2) = 240$
$(d+4)(x-2) = dx$
$dx - 2d + 4x -8 = dx$ (/2)
$2x - d = 4$
$d = 2x - 4$

$(2x - 4)x = 240$
$2x^2 - 4x - 240 = 0$ (/2)
$x^2 - 2x - 120 = 0$

Soma: $(-10)+12=2$
Produto: $(-10)*12=-120$
$x_1=-10$, $x_2 = 12$ dias

$d = 24 - 4 => d=20km/dia$

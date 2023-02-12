tags: #estudos/matemática 

- Operação inversa da potenciação

- Termologia
$\sqrt[n]{a}$
n = Índice
$\sqrt{}$ = Radical
a = Radicando

- Definição
> Seja *a* um número real e *n* um número >= 2. Dizemos que $\sqrt[n]{a}$ é um número *b*, tal que $b^n = a$.

- Exemplos
	1. $\sqrt[3]{-8} = -2 => (-2)3 = -8$ 
	2. $\sqrt[2]{25} = 5 => 5^2 = 2$

# Notas
1. Da definição temos que $\sqrt[n]{a^n} = a$, para todo a >= 0.
2. Raiz quadrada de um número perfeito:
	- $\sqrt[2]{a^2} = |a|$, no qual $|a| =$ a, se a >= 0
						    -a, se a < 0	
	- Raiz quadrada de um valor elevado ao quadrado, o resulado é o **módulo** do valor a.
3. $x^2 - 49 = 0$ 
	- $\sqrt[2]{x^2} = \sqrt{49} = |x| = (x1=7, x2=-7)$
4. Se o índice for par, o radicando deve ser maior ou igual a 0. Se for impar o radicando pode ser qualquer número, ou seja, pertence aos **reais**.

- Exemplos
	1. $\sqrt[2]{(-2)^2} = |-9| = 9$ 
	2. $\sqrt{(3 - \sqrt{2})}= |3-\sqrt{2}| = 3 -\sqrt{2}$ 
	3. $\sqrt{(2 - \sqrt{5})} = |2-\sqrt{5}| = \sqrt{5} - 2$ 

# Potência de Expoente Racional
- Definição
> A potência de base *a* (*a* > 0), e expoente racional $\frac{m}{n}$, é o número:
> $$a^{\frac{m}{n}} = \sqrt[n]{m}$$
- Exemplos
	1. $3^{\frac{3}{2}} = \sqrt[2]{3^3} = \sqrt{27}$  
	2. $5^{\frac{5}{2}} = \sqrt{5^5}$ 

# Propriedades
- p1: $\sqrt[n]{a * b} = \sqrt[n]{a} * \sqrt[n]{b}$
	- $\sqrt{12} = \sqrt{2^2 * 3} = \sqrt{2^2}*\sqrt{3} = 2\sqrt{3}$ 
	- Como nossa raiz é **quadrada**, na fatoração formamos pares de números iguais. Os que formarem um par, fica fora da raiz, já os que sobraram, ficam dentro.
	- $\sqrt[3]{864} = 2*3\sqrt[3]{4} = 6\sqrt[3]{4}$
		- ![[Pasted image 20230204200303.png]]
	- Caso a raiz seja cúbica, teremos que formar trios.
- p2: $\sqrt[n]{\frac{a}{b}} = \frac{\sqrt[n]{a}}{\sqrt[n]{b}}$ 
	- Calcule o valor da expressão $\frac{\sqrt[4]{32}}{\sqrt[4]{2}} + \frac{\sqrt[3]{192}}{\sqrt[3]{3}} = \sqrt[4]{\frac{32}{2}} + \sqrt[3]{\frac{192}{3}} = \sqrt[4]{16} + \sqrt[3]{64} = \sqrt[4]{2^4} + \sqrt[3]{4^3} = \boxed{2+ 4=6}$ 
- p3: $(\sqrt[n]{a})^m = \sqrt[n]{a^m}$
	- $(\sqrt[4]{16})^2 = \sqrt[4]{16^2} = \sqrt[2]{16^1} = 4$ 
- p4: $\sqrt[n]{a^m} = \sqrt[n \times p]{a^{m \times p}}$ 
	- Coloque os seguintes números em ordem crescente:
	- $\sqrt[3]{3}, \sqrt[4]{5}, \sqrt[6]{7}$
	- $\sqrt[12]{3^4}, \sqrt[12]{5^3}, \sqrt[12]{7^2}$ 
	- $\sqrt[12]{81}, \sqrt[12]{125}, \sqrt[12]{49}$
	- $\boxed{\sqrt[6]{7} < \sqrt[3]{3} < \sqrt[4]{5}}$ 
- p5: $\sqrt[m]{\sqrt[n]{a}} = \sqrt[m \times n]{a}$  
	- Simplifique: $\frac{\sqrt{2 \sqrt[3]{16}}}{\sqrt[3]{2 \sqrt{8}}} = \frac{\sqrt{\sqrt[3]{2^3 \times 16}}}{\sqrt[3]{\sqrt{2^2 \times 8)}}} = \frac{\sqrt[6]{8 \times 16}}{\sqrt[6]{4 \times 8}} = \sqrt[6]{\frac{8 \times 16}{4 \times 8}} = \sqrt[6]{4} = \sqrt[6]{2^2} = \sqrt[3]{2}$ 
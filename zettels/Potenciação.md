tags: #estudos/matemática 

- Termologia
$a^b$

a = Base
b = Expoente

- Definição
> Seja *a* um número real e *n* um número natural, com n >= 2. A potência de base *a* e expoente *n* é o número $a^n$ tal que:
![[Pasted image 20230204002107.png]]

- Exemplos
	1. $(-5)^2 = (-5) * (-5) = 25$
		- Número de expoente par com base negativa, resultado positivo. 
	2. $-5^2 = -5 * 5 = -25$
	3. $-2^3 = -2 * 2 * 2 = -8$
	4. $-(-2)^3 = -(-2^3) = 8$
	5. $(\frac{3}{2})^2 = \frac{3^2}{2^2} = \frac{9}{4}$
	6. $-(-\frac{3}{2})^3 = -(-\frac{27}{8}) = \frac{27}{8}$ 
	7. $(-1)^{10} = 1$
	8. $(-1)^{15} = -1$
		- Número de expoente impar com base negativa, resultado negativo. 

- Definição
> Seja *a* um número real não nulo e *n* um número natural, com *n* >= 2. A potência de base *a* e expoente *-n* é o número $a^{-n}$ tal que:
![[Pasted image 20230204004236.png]]

- Exemplos
	1. $4^{-2} = \frac{1}{4^2} = \frac{1}{16}$
	2. $(\frac{3}{2})^{-3} = \frac{2^3}{3^3} = \frac{8}{27}$ 
	3. $-(\frac{1}{2})^{-4} = -2^4 = -16$
	4. $10^{-5} = \frac{1}{10^5} = \frac{1}{100000} = 0,00001$  
	5. $(\frac{1}{10})^{-6} = 10^6 = 1.000.000$

# Notas
1. Toda potência de expoente 1 é igual à base.
$$a^1 = a$$
2. Para a != 0:
$$a^0 = 1$$
# Propriedades
- Se a, b pertencem aos **números reais** e m, n pertencem aos **números naturais**, valem as seguintes propriedades:

- p1: $a^m \times a^n = a^{m + n}$
	- $\frac{2 * 3^6 + 3^7}{3^4 - 3 * 3^5} = \frac{2 * 3^2 * 3^4 + 3^3 * 3^4}{3^4 - 3 * 3^1 * 3^4} = \frac{3^4(18 + 27)}{3^4(1 - 9)} = \boxed{\frac{45}{-8} = \frac{-45}{8} = -\frac{45}{8}}$  
	- Frações negativas podem ser escritas das 3 formas. O resultado é o mesmo.
- p2: $\frac{a^m}{a^n} = a^{m-n}$ 
	- Simplifique: $\frac{a^{2(n + 1)} * a^{3 - n}}{a^{1 - n}} = \frac{a^{2(n + 1) + 3 - n}}{a^{1 - n}} = \frac{a^{2n + 2 = 3 - n}}{a^{1-n}} = \frac{a^{n + 5}}{a^{1-n}} = a^{n + 5 -1 + n} = \boxed{a^{2n + 4}}$   
- p3: $(a^m)^n = a^{m*n}$ 
	- Assinale V para verdadeiro e F para falso nos itens abaixo:
	- ( V ) $4^{3000} < 3^{4000} => (4^3)^{1000} < (3^4)^{1000} => 64^{1000} < 81^{1000}$  
	- ( F ) $(-2^3)^2 = (-2^2)^3 => (-8)^2 = (-4)^3 => \boxed{64 =! -64}$ 
- p4: $(a * b)^n = a^n * b^n$
	- Quantos algarismos possui o número $5^8 \times 4^3$?
	- $3^8 * (2^2)^3 =5^2 * 5^6*  2^6 = 5^2(5 * 2)^6 = 5^2 * 10^6 = 25*1.000.000 = 25.000.000$
	- R: $\boxed{8}$
- p5: $(\frac{a}{b})^n = \frac{a^n}{b^n}$
	- Assinale V para verdadeiro e F para falso nos itens abaixo:
	- ( V ) $\frac{6^4}{2^6} = (\frac{9}{2})^2$ = $\frac{6^4}{2^6} = \frac{6^4}{2^2*2^4} = \frac{1}{4}(\frac{6}{2})^4 = \frac{3^4}{4}= \frac{81}{4}$
	- ( F ) $\frac{6^4}{4*3^4} = 2$ = $\frac{1}{4}(\frac{6}{3})^4 = \frac{2^4}{4} = \frac{16}{4} = 4$ 
tags: #estudos/matemática 

- Termologia
- Capital (C)
- Tempo (t)
- Juros (j)
- Taxa (i)
- Montante (M) = C + J

- Exemplo
![[Pasted image 20230212150450.png]]
C = R$ 1.000,00
T = 3 anos
i = 10% a.a

1º ano: $1000+\frac{10}{100}*1000 = 1000+100 = 1100$
2º ano: $1100+\frac{10}{100}*1000 = 1100+100 = 1200$
3º ano: $1200+\frac{10}{100}*1000 = 1200 + 100 = 1300$
M = R$ 1.300,00

- De modo geral, podemos dizer que:
> Quando um capital **C** é aplicado durante **t** unidades de tempo e a taxa **i** de juros, por unidade de tempo, incide apenas sobre o capital inicial, os juros **j** são chamados de **juros simples**. Esses juros ao final da aplicação são calculados por:

$$j = C*i*t$$
$j = 1000*\frac{10}{100}*3 => j=300$
M = 1000 + 300 => M = R$ 1.300,00

- Exemplo
- Qual é o juro simples produzido por um capital de R$ 1.200,00 aplicado durante um ano e meio à taxa de 4% ao mês?
	- $j = 1200*\frac{4}{100}*18 =$ $864$
	- Há duas formas de fazer, convertendo o ano para meses ou convertendo a taxa para ano, multiplicando por 12.
- Em quanto tempo se pode duplicar um capital aplicado a juro simples à taxa de 0,1% ao dia?
	- t = ? (dias)
	- i = 0.1% a.d
	- M = C + j = C + C = 2C
	- j = C.i.t
	- $C = C*\frac{0,1}{100}*t$
	- $\frac{0,1}{100}*t = 1$
	- $0,1t = 100$
	- $\frac{1}{10}t = 100$
	- $t = 1000$ dias

# Juros compostos
- Exemplo
![[Pasted image 20230212182403.png]]
C = R$ 1.000,00
t = 3 anos
i = 10% a.a

1º ano: $1000 + \frac{10}{100}*1000 = 1100$
2º ano: $1100 + \frac{10}{100}*1100 = 1210$
3º ano: $1210 + \frac{10}{100}*1210 = 1331$
M = R$ 1.331,00

## Fórmula
| | Início | Juros | Montante |
| - | - | - | - |
| 1º Período | C | iC | $1C + iC = C(1+i)$ |
| 2º Período | $C(1+i)$ | $i*C(1+i)$ | $1*C(1+i) + i*C(1+i)$; $C(1+i)(1+i) = C(1+i)^2$ |
| 3º Período | $1*C(1+i)^2$ | $i*C(1+i)^2$ | $C(1+i)^2(1+i)^1 = C(1+i)^3$ |
- Logo
$$M = C(1+i)^t$$
- Exemplo
- Determine os juros compostos gerados por uma aplicação de R$ 4.000,00 por um período de um ano e meio, à taxa de 8% ao mês. dado: $(1,08)^{18} = 3,99$.
	- j = ? 
	- C = 4000
	- i = 8% a.m
	- t = 18 meses
	- $M = C(1+i)^t$
	- $M = 4000(1+0,08)^{18}$
	- $M = 4000*(1,08)^{18}$
	- $M = 4000*3,99$
	- $M = 4*1000*3,99$
	- $M = 4*3990$
	- $M = 15960$
	- $J = M-C$
	- $15960 - 4000 = 11960$
- Apliquei um capital de R$ 10.000,00 durante 3 anos, a juro composto. A taxa de juro no primeiro ano foi de 10%, no segundo, 12% e no terceiro, 8%. Qual foi o montante acumulado nos 3 anos?
	- $[(10000*1,1)*1,12]*1,08$
	- $10000*\frac{11}{10}*\frac{112}{100}*\frac{108}{100} = 13.305,60$

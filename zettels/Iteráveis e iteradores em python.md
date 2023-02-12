tags: #programação/python  
status: #zettel/fleeting

# Iterável (iterable)
- É o item que é iterado, ou seja, ele vai distribuir os valores.
- Tem a responsabilidade de somente deter os valores.
- Itens iteráveis em Python incluem sequências (como listas, tuplas e strings) e coleções (como dicionários e conjuntos).
```Python
iterable = ['eu', 'tenho', '__iter__']
```

# Iteradores (iterator)
- É o objeto que itera, ou seja, ele vai receber um valor por vez.
- Tem a responsabilidade de **somente**, saber qual o próximo valor.
- Utiliza-se a função iter ou  o próprio "for".
```Python
iterator = iter(iterable)
```

# Generator
- Todo generator é um iterator, mas nem todo iterator é um generator.
- É uma função que trava.
- Bem mais leve que uma lista.

- Diferença de tamanho, em bytes, de uma list comprehension e um generator:
```Python
import sys

lista = [x for x in range(1000)]
gerador = (x for x in range(1000))

print(sys.getsizeof(lista))
print(sys.getsizeof(gerador))
-----------------------------------------
8856
104
```
- Um gerador não guarda uma lista inteira, ele guarda um valor de cada vez. Podendo ser executado pela função "next()", assim retornando um valor por vez.
- Então, basicamente o valor da lista está todo na memória, e o do generator está **esperando**, uma função, para retornar o próximo valor.

## Generator function
- Uma generator function vai pausar, e esperar ser chamada, assim retornando um valor por vez.
- Você pode definir uma função dessa, simplesmente colocando a palavra privada "yield".
```Python
def generator(n=0):
    yield 1  # Pausar
    return 'Acabou'
  
gen = generator(n=0)
print(next(gen))
-----------------------------
1
```
- Perceba que a funçõa somente retornou o "yield", por causa que passei uma função iteradora (next()), para receber o próximo valor. Ou seja, ele vai ==parar== a função no "yield".

- Podemos criar uma função igual a "range()".
```Python
def generator(n=0, max=10):
    while True:
        yield n
        n += 1

        if n >= max:
            return
  

gen = generator(max=1000)
for n in gen:
    print(n)
```
- Ira retornar de 0 - 999.

### Como checar se é um generator
- Precisamos importar a classe "GeneratorType" de types.
- `from types import GeneratorType`.
- Em seguida, printamos usando a função "isinstance()", que vai retornar um valor booleano, se é ou não um generator.
```Python
from types import GeneratorType

generator = (x for x in range(10))
print(isinstance(generator, GeneratorType))
--------------------------------------------
True
```

### Debugando
#### 1 frame
![[Pasted image 20230112193255.png]]

#### 2 frame
![[Pasted image 20230112193350.png]]

#### 3 frame
![[Pasted image 20230112193418.png]]

#### 4 frame
![[Pasted image 20230112193437.png]]

#### 5 frame
![[Pasted image 20230112193448.png]]

#### 6 frame
![[Pasted image 20230112193501.png]]

#### 7 frame
![[Pasted image 20230112193518.png]]



# References
- [Curso de Python do Luiz Otávio Miranda](https://www.udemy.com/user/luiz-otavio-miranda)
	- Sec. 4 ep. 145.

tags: #programação/python/funções 
status: #zettel/fleeting
# O que são funções decoradoras
- Um função decoradora, é uma função que decora outras funções (decorar = adicionar, remover, restringir e alterar).

## Exemplo de função decoradora
```Python
def criar_funcao(func):
    def interna(*args, **kwargs):
        print('Vou te decorar')
        for arg in args:
            e_string(arg)
        resultado = func(*args, **kwargs)
        print(f'O seu resultado foi {resultado}.')
        print('Ok, agora você foi decorada')
        return resultado
    return interna

@criar_funcao
def inverte_string(string):
    return string[::-1]


def e_string(param):
    if not isinstance(param, str):
        raise TypeError('param deve ser uma string')



invertida = inverte_string('123')
print(invertida)
----------------------------------------------------
Vou te decorar
O seu resultado foi 321.
Ok, agora você foi decorada
321
```
- Perceba que no momento que eu decorei a função com o *syntax sugar* "@criar_funcao", a função é executada e, troca altomaticamente, o nome "inverte_string", para a função interna do "criar_funcao", que é a "nested function", chamada no código de "interna".
- "criar_funcao" é uma ==fábrica de funções==.
- A função interna é chamada de "inner function" ou "nested function".

## Exemplo de função decoradora que recebe parâmetros
```Python
def fabrica_de_decoradores(a=None, b=None, c=None):
    def fabrica_de_funcoes(func):
        print('Decoradora 1')

        def aninhada(*args, **kwargs):
            print('Parâmetros do decorador, ', a, b, c)
            print('Aninhada')
            res = func(*args, **kwargs)
            return res
        return aninhada
    return fabrica_de_funcoes


@fabrica_de_decoradores(1, 2, 3)
def soma(x, y):
    return x + y


decoradora = fabrica_de_decoradores()
multiplica = decoradora(lambda x, y: x * y)

dez_mais_cinco = soma(10, 5)
dez_vezes_cinco = multiplica(10, 5)
print(dez_mais_cinco)
print(dez_vezes_cinco)
------------------------------------
Decoradora 1
Decoradora 1
Parâmetros do decorador,  1 2 3
Aninhada
Parâmetros do decorador,  None None None
Aninhada
15
50
```
1.  A função `aninhada` retorna o resultado `res`
2.  A função `fabrica_de_funcoes` retorna a função aninhada
3.  A função `fabrica_de_decoradores` retorna a função `fabrica_de_funcoes`

# Closure
- Toda função decoradora é uma closure.
- São funções que geram outras funções. Ou seja, uma ==fábrica de funções==.
- Em python, uma closure é uma função que "lembra" do ambiente (ou escopo) em que ela foi criada. Isso significa que, mesmo quando a função é chamada fora desse escopo, ela ainda tem acesso às variáveis ​​e outros recursos que existiam no momento em que foi criada.
- Uma closure é ==criada== quando uma ==função dentro de outra função tem acesso às variáveis ​​da função externa==. A função interna é capaz de "lembrar" dessas variáveis ​​mesmo quando a função externa já terminou de executar.

```python
def criar_multiplicador(multiplicador):
    def multiplicar(numero):
        return numero * multiplicador
    return multiplicar
  

duplicar = criar_multiplicador(2)
triplicar = criar_multiplicador(3)
quadriplicar = criar_multiplicador(4)

print(duplicar(4))
print(triplicar(4))
print(quadriplicar(4))
-----------------------------------------
8
12
16
```

# References
- [Curso de Python do Luiz Otávio Miranda](https://www.udemy.com/user/luiz-otavio-miranda)

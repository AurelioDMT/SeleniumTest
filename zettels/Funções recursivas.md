tags: #programação/python/funções 

# O que é uma função recursiva?
- Basicamente, é uma função que retorna ela mesma.
- Necessário de um **caso base**, caso passe de 1000 execuções, o python lança uma exceção ([[Tratando exceções em python]]).
- Caso base: limitador, com objetivo de parar a função.
```Python
def fatorial(n):
    if n <= 1:
        return 1
    
    return n * fatorial(n - 1)
```

# Vantagens da recursão
-   Funções recursivas fazem o código parecer limpo e elegante.
-   Uma tarefa complexa pode ser dividida em sub-tarefas mais simples usando recursão.
-   Gerar uma sequência é consideravelmente mais fácil com recursão do que usando alguma iteração aninhada(`for/while` dentro de outro `for/while`).


# Reference
- [Curso de Python do Luiz Otávio Miranda](https://www.udemy.com/user/luiz-otavio-miranda)
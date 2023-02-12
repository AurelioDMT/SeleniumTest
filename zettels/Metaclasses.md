tags: #programação/python 

- O termo "metaprogramação", refere-se ao programa que tem o conhecimento de manipular ele mesmo. Python suporta "metaprogramação" para classes, chamada de **metaclasses**.
- Raramente é usada.

# O que é uma metaclasse?
- É a classe que está acima de object.
- A classe que cria outras classes.
- Em python, usa-se a metaclasse "type".
```Python
Foo = type('Foo', (object,), {})
f = Foo()
```
- Primeiro é declarado o tipo da classe, depois a herança padrão, ai o dict da classe.

## Ao criar uma classe, coisas ocorrem por padrão nessa ordem
1. `__new__` da metaclass é chamado e cria a nova classe.
2. `__call__` da metaclass é chamado com os argumento e chama:
	- `__new__` da class com os argumentos (cria a instância).
	- `__init__` da class com os argumentos.
3. `__call__` da metaclass termina a execução.

# Métodos importantes da metaclasse
- `__new__(mcs, name, bases, dct)` (cria a classe).
- `__call__(cls, *args, **kwargs)` (cria e inicializa a instância)

# Reference
- [Curso de Python do Luiz Otávio Miranda](https://www.udemy.com/user/luiz-otavio-miranda)
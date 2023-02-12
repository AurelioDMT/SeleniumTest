tags: #programação/python 

```Python
class A(object):
	...

class B(A):
	...
```
- Diferente da relação de classes de composição, que, associação: usa um objeto, agregação: tem um objeto, composição: é dono de um objeto. A herança é o objeto.

- Quando criada uma classe em python, cria-se um tipo diferente de dado. Quando uma classe é herdada, ela é o tipo da classe **super** (classe principal).
	- Classe principal, que herda, também chamada de: super class, base class e parent class.
	- Classe filha, que é herdada, também chamada de: sub class, child class e derived class.

- Toda classe em python herda altomaticamente de um built in, chamado object. Que é um objeto vazio.

# Pra que serve a herança?
- Para generalizar uma classe específica. Abstrair. Poder usar essa classe em outras.

# Sobreposição de membros
- Quando um objeto é herdado, todos os seus métodos públicos também são.
- Métodos podendo ser sobreescritos.
- Você pode chamar o método da classe pai, usando o a classe "super()".
```Python
class MinhaString(str):
    def upper(self):
        print('Qualquer modificação')
        super(MinhaString, self).upper()

```
- "MinhaString" herda de str, que tem o método "upper". Quando chamado pela "MinhaString", ele  vai executar o *print* e a função pai, que deixa a string em caixa alta.

- Exemplo de código com herança simples e múltipla: [[exemplo mixin]]

# Reference
- [Curso de Python do Luiz Otávio Miranda](https://www.udemy.com/user/luiz-otavio-miranda)
tags: #programação/python 

- Para fazer uma abstração, é necessário importar a classe "ABC" (Abstract Base Class) da biblioteca "abc".
- Você vai criar uma classe e herdar ela de "ABC". Pra uma classe ser abstrata, ela PRECISA de um método abstrato, então junto com a classe, importamos também o "staticmethod".
- Classes abstratas não podem ser instanciáveis.
- Classes abstratas podem ter métodos abstratos e métodos concretos.
- Métodos abstratos serão obrigatórios para cada classe filha. E devem ser implementados.
- Classes abstratas tem sua metaclass sendo "ABCMeta".

# Reference
- [Curso de Python do Luiz Otávio Miranda](https://www.udemy.com/user/luiz-otavio-miranda)
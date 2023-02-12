tags: #programação/python 

- Para usarmos uma dataclasse, precisamos importar da biblioteca dataclasses. 
- `from data classes import data class`.

# O que é uma dataclasse?
- É uma classe normal, com alguns métodos mágicos implementados, mas com syntax sugar. Ou seja, masi fácil de se digitar.

- Exemplo de dataclasse:
```Python
from dataclasses import dataclass


@dataclass
class Pessoa:
    nome: str
    sobrenome: str
```

# Pra que serve uma dataclasse?
- Pra facilitar o processo de criação de classe. Já que, já vem com alguns métdos mágicos como, init, repr e equal, não precisamos implementá-los.

- É bastante flexível, você pode passar parâmetros para o decorador, mudando o comportamento da classe.

# Field
- Serve para colocar valores mutáveis na sua dataclasse e, manusear os campos.
```Python
from dataclasses import dataclass, field


@dataclass
class Pessoa:
    nome: str = field(
        default='FAZOL', repr=False
    )
    sobrenome: str = 'sobrenome'
    idade: int = 0
    enderecos: list[str] = field(default_factory=list)
```
- Nesse código, usei o field no "nome" para definir um valor padrão e tirar ele do repr.
- Também usei no "enderecos", que no caso é um lista, mutável. A factory serve para criar uma lista diferente para cada instância da classe.

# Reference
- [Curso de Python do Luiz Otávio Miranda](https://www.udemy.com/user/luiz-otavio-miranda)
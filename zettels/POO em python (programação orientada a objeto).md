tags: #programação/python 
status: #zettel/fleeting

# Composição
- A linguagem python inteira é formada por objetos, variáveis, funções, módulos etc.
- Objetos são instancias de classes.
- Classes são **moldes** para criar objetos
- Classes vão ter atributos e métodos

## Quatro pilares da programação orientada a objetos
1. [[Abstração]]
2. [[Herança]]
3. [[Encapsulamento]]
4. [[Polimorfismo]]

# Parâmetro self
- O primeiro parêmetro de todo método que vai tratar a instância, tem que ser **self**.
- Self, refere-se a instância da classe.
- Parâmetros com self, são parâmetros de **instância**.
```Python
class Pessoa():
    def __init__(self) -> None:
        pass
```

# Métodos em classe
- Métodos são funções dentro de classe, caracteriza-se em 3 diferentes métodos:
	1. Método de instância (method)
	2. Método de classe (classmethod)
	3. Método estático (staticmethod)

## Exemplo de método de classe
```Python
class Connection:
    def __init__(self, host='localhost') -> None:
        self.host = host
        self.user = None
        self.password = None

    def set_user(self, user):
        self.user = user
    
    def set_password(self, password):
        self.password = password

    @classmethod
    def create_with_auth(cls, user, password):
        connection = cls()
        connection.user = user
        connection.password = password
        return connection
```
- No método "create_with_auth", recebe usuário e senha. Como refere-se a classe, primeiro eu instancio uma variável com a própria classe. Depois eu seto os parâmetros e retorno a instância da classe, assim, criando uma classe apartir de um método.
	- `conec = Connection.create_with_auth('Lucas', 1234)`

# Getters e setters
- Como toda linguagem de programação, getters são para obter um valor privado, e o seter é para modificar o valor.

## Getter
- Em python, temos as **@propertys**, que você pode utilizar como um getter. Decorando a função com o nome.
- Ela é um método que se comporta como um atributo.
```Python
class Caneta:
    def __init__(self, cor) -> None:
        self.cor_tinta = cor

    @property
    def cor(self):
        return self.cor_tinta
```
- `caneta = Caneta()
- `caneta.cor`

### Pra que que serve o getter?
1. Pra evitar quebrar o código cliente
2. Para habilitar o setter.
3. Para executar ações ao obter um atributo.

## Setter
- Com um getter, você abilita o setter.
- É passado também como um decorador.
- Sintaxe: `@{nome_getter}.setter`.
- Serve para atribuir um valor.
```Python
class Caneta:
    def __init__(self, cor) -> None:
        self.cor = cor

    @property
    def cor(self):
        return self._cor
    
    @cor.setter
    def cor(self, valor):
        self._cor = valor
```
- `caneta = Caneta()`
- `caneta.cor = 'Rosa'`

# Relações entre classes (composição)
- Relação fraca: Objeto existe independente de outro.
- Relação forte: Objeto gerencia o ciclo de vida de outro.

## Associação (relação fraca)
- É um tipo de relação onde objetos estão ligados no sistema.
- É a relação mais comum entre objetos.
- Geralmente, temos uma associação quando um objeto tem um atributo que referencia outro objeto.
- A associação não especifica como um objeto controla o ciclo de vida de outro.
```Python
class Escritor:
    def __init__(self, nome) -> None:
        self.nome = nome
        self._ferramenta = None
    
    @property
    def ferramenta(self):
        return self._ferramenta

    @ferramenta.setter
    def ferramenta(self, ferramenta):
        self._ferramenta = ferramenta


class FerramentaDeEscrever:
    def __init__(self, nome) -> None:
        self.nome = nome

    def escrever(self):
        return f'{self.nome} está escrevendo.'


escritor = Escritor('Luiz')
ferramenta_de_escrever = FerramentaDeEscrever('Caneta Bic')
escritor.ferramenta = ferramenta_de_escrever
print(escritor.ferramenta.escrever())
-----------------
Caneta Bic está escrevendo.
```
- Nesse código, há um getter e um setter. O getter retorna o atributo privado quando é chamado. O setter, seta a ferramenta.
- Quando feita associação, uma classe consegue usar os métodos de outras.

## Agregação (relação fraca)
- A *agregação* é uma especialização da **associação**. Ou seja, é um tipo de associação.
- Geralmente é uma relação de um para muitos ([[one-to-many]]).
- Os objetos podem viver separadamente, mas pode se tratar de uma relação onde um objeto precisa de outro para fazer determinada tarefa.
- (existem controvérsias sobre as definições de agregação).
```Python
class Carrinho:
    def __init__(self) -> None:
        self._produtos =  []
    
    def total(self):
        return  sum([p.preco for p in self._produtos])

    def listar_produtos(self):
        print()
        for produto in self._produtos:
            print(produto.nome, produto.preco)
        print()

    def adicionar_produto(self, *produtos):
        # self._produtos += produtos
        self._produtos.extend(produtos)


class Produto:
    def __init__(self, nome, preco) -> None:
        self.nome = nome
        self.preco = preco


carrinho = Carrinho()
p1 = Produto('Chocolate', 6.99)
p2 = Produto('Papel higiênico', 17)
```
- Esse é um código de agregação, onde o produto agrega ao carrinho,ou seja, carrinho de compras TEM produto, mas podendo viver separademente. 

## Composição (relação forte)
- A *composição* é uma especialização da **agregação**. Ou seja, é um tipo de agregação.
- Quando um objeto é deletado, todos os que estão em composição com ele, também são.
```Python
class Cliente:
    def __init__(self, nome) -> None:
        self.nome = nome
        self.enderecos = list()
    
    def inserir_endereco(self, rua, numero):
        self.enderecos.append(Endereco(rua, numero))

    def listar_enderecos(self):
        for endereco in self.enderecos:
            print(endereco.rua, endereco.numero)

    
class Endereco:
    def __init__(self, rua, numero) -> None:
        self.rua = rua
        self.numero = numero
```
- O objeto "endereco" é deletado caso o objeto "Cliente" for excluido, porque, na função "inserir_endereco", está **instanciando** a classe. Logo quando deletada a instância (referência), a classe é deletada junto.

# Dicas
## função vars()
- Use-a em uma instância de função, para retornar um dicionário contendo todos os seus atributos.
```Python
class Pessoa:
    def __init__(self, nome, idade) -> None:
        self.nome = nome
        self.idade = idade
    

p = Pessoa('Luiz', 21)
print(vars(p))
-----------------------------------------------
{'nome': 'Luiz', 'idade': 21}
```

# References
- [Curso de Python do Luiz Otávio Miranda](https://www.udemy.com/user/luiz-otavio-miranda)

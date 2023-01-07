tags: #programação/sql 
status: #zettel/fleeting

![[Diagrama exemplo.png]]
- Esse diagrama é basicamente uma <b>abstração</b> da parte do sistema que criaremos.

# O porquê de ser apenas uma abstração
- Programadores customam abstrair um pequeno trecho de um programa, que poderia ser maior.

# Do que este diagrama fala?
- Ele fala de **entidades** e o *relacionamento* entre elas.

# Entidades
- As <b>entidades</b> é representada por retângulos no diagrama. Cada retângulo é uma tabela, em cada tabela haverá atributos, que chamamos de <b>colunas</b>.

```tx
|||                       Users           ||
PK  | ID |
 ------------ | ----------- | -----------|
                     | first_name
       | last_name
       | email
       | password_hash                            

```
- No caso desta tabela são: id, first_name, last_name, email, password_hash.
- Pode haver inúmeros atributos, porém, este caso se trata de uma <b>abstração</b>, isto é, você só vai passar o que é importante.

# Primary Key (PK)
- Cada tabela terá sua <b>Primary Key</b>, isto serve para indentificar índices na tabela.
![[tabela users exemplo.png]]
- Por exemplo, quando eu for apagar ou editar alguém desta tabela, eu vou fazer isso pelas <b>Primary Keys</b> (que estão em vermelho).

- Se você define uma <b>Primary Key</b> na tabela, você terá as seguntes restrições:
	- O valor desta chave, sempre vai ser único
	- O valor não pode ser nulo
	- Não posso ter outra **Primary Key** na tabela

- A maneira mais simples de se criar uma <b>Primary Key</b> é com <i>auto-increment</i>, como está na tabela acima, id 1... 2... etc.
- Desse jeito, sendo apagadas, elas continuaram contanto. Isto deixará "furos", que pode ser muito importante conte-los.
- Por exemplo, se eu apagar a 97, e a tabela tem 500, a próxima adicionada será a 501, e a 97 ficará vazia.

- O mais comúm de usar é a <b>Surrogate Key</b>, que é uma chave artificial e auto incremental, a chamamos de artificial porque ela não existe em lugar nenhum, não é uma chave natural, é simplesmente criada.

# Foreign Key (FK)
- Em português "chave-estrangeira", que vai fazer referência a <b>Primary Key</b> de outra tabela.
![[tabela profiles exemplo.png]]
- Tal como, essa tabela está ligada a outra. O <b>Foreign Key</b> dela é a coluna "user_id", referenciando diretamente com a <b>Primary Key</b> da tabela "users".

# Relacionamento
- As relações são as linhas no diagrama, a gente pode ter 3 tipos de relações
	- Relações de um para um ([[one-to-one]]).
	- Relações de um para muitos ([[one-to-many]]).
	- Relações de muitos para muitos ([[many-to-many]]).

# Continuação (de acordo com o curso)
- [[Criando uma base de dados simples com Docker e DBeaver]]

# References
- [Curso de Python do Luiz Otávio Miranda](https://www.udemy.com/user/luiz-otavio-miranda)
	- Sec. 20 ep. 485 - 491.

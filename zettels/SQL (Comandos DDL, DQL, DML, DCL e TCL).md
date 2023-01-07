tags: #programação/sql 
status: #zettel/fleeting

- SQL (Structured Query Language) como conhecemos é a linguagem usada por base de dados, podemos performar certas operações em uma base de dados existente e também, criar uma nova base de dados.
- Esses comandos SQL são principalmente caracterizados em cinco categorias como:
	1.  DDL – Data Definition Language
	2.  DQL – Data Query Language
	3.  DML – Data Manipulation Language
	4.  DCL – Data Control Language
	5.   TCL – Transaction Control Language

# DLL (Data Definition Language)
- DLL consiste nos comandos SQL que podem ser utilizados para definir o esquema da base de dados.
- DDL é um conjunto de comandos SQL utilizados para criar, modificar e eliminar estruturas de base de dados, mas não dados. Estes comandos não são normalmente utilizados por um utilizador geral, que deveria estar a ter acesso à base de dados através de uma aplicação.

- Lista de comandos DDL
	- CREATE: Esse comando é usado para criar base de dados ou seus objetos (tabela, índices, funcções, vizualizações, procedimentos de loja e accionadores).
	- DROP: Esse comando é usado para deletar objetos da base de dados.
	- ALTER: Esse comando é usado para alterar a esturtura de uma base de dados.
	- TRUNCATE: Isto é utilizado para remover todos os registos de uma tabela, incluindo todos os espaços atribuídos para os registos são removidos.
	- COMMENT: Isto é utilizado para adicionar comentários ao dicionário da base de dados.
	- RENAME: Isto é utilizado para renomear um objeto existente na base de dados.

# DQL (Data Query Language)
- As declarações DQL são utilizadas para realizar consultas sobre os dados dentro de objectos de esquema. Podemos definir DQL da seguinte forma: é um componente da instrução SQL que permite obter dados da base de dados e impor-lhe ordem.

- Lista de comandos DQL
	- SELECT: É usado para recuperar dados da base de dados.

# DML (Data Manipulation Language)
- Trata da manipulação de dados presente na base de dados. É o componente da instrução SQL que controla o acesso aos dados à base de dados. Basicamente, as instruções DCL são agrupadas com instruções DML.

- Lista de comandos DML
	- INSERT: É usado para inserir dados à uma tabela.
	- UPDATE: É usado para atualizar dados existente em uma tabela.
	- DELETE: É utilizado para apagar registos de uma tabela de uma base de dados.
	- LOCK: Controle de tabela sumiltâneo.
	- CALL: Chama um subprograma PL/SQL ou JAVA.
	- EXPLAIN PLAN: Descreve o caminho dos dados.

# DCL (Data Control Language)
- DCL inclui comandos como GRANT e REVOKE que lidam principalmente com os direitos, permissões e outros comandos do sistema de base de dados.

- Lista de comandos DCL
	- GRANT: Esse comando da acesso ao usuário aos privilégios da base de dados.
	- REVOKE: Este comando retira os privilégios de acesso do utilizador, atribuído através da utilização do comando GRANT.

# TCL (Transaction Control Language)
- As transações agrupam um conjunto de tarefas numa única unidade de execução. Cada transação começa com uma tarefa específica e termina quando todas as tarefas do grupo são concluídas com sucesso. Se alguma das tarefas falhar, a transação falha. Por conseguinte, uma transação tem apenas dois resultados: sucesso ou fracasso.

- Lista de comandos TCL
	- COMMIT: Comita a transação.
	- ROLLBACK: Reverte uma transação caso algum erro ocorra.
	- SAVEPOINT: Atribui um savepoint dentro de uma transação.
	- SET TRANSACTION: Especifica características para a transação.

# References
- https://www.geeksforgeeks.org/sql-ddl-dql-dml-dcl-tcl-commands/

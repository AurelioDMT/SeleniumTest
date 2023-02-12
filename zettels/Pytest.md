tags: #programação/python/framework
status: #zettel/fleeting
doc: https://docs.pytest.org/en/7.2.x/

- Pytest é um framework em python, que facilita a você executar os testes.
- É o framework mais usado no ramo de testes em python.
- Não vem na biblioteca padrão.

# Configurar seu ambiente de testes
- Primeiro de tudo, importar o módulo pytest.
	- `pip install pytest`

- Me organizo utilizanod 2 pastas, uma pra por os códigos de testes e outra para os que vão ser testados.
	- Primeira pasta "tests", precisa ser esse nome, para o pytest indentificar, ali vai ficar seus módulos de teste. Os módulos também seguem um padrão de nome: `test_{nome}.py`.
	- Segunda pasta, você tem a liberdade de botar os nomes que quiser, MAS LEMBRA, a pasta teu que ser um pacote, então basta adicionar um módulo vazio chamado: `__init__.py`.
![[Pasted image 20230118011959.png]]

# Fazendo testes
- Já estruturado seu ambiente de testes, agora é só codar seus testes e depois executar o seguinte comando no terminal: `pytest`

- Você também pode debugar ([[Debug]]) o código que deu erro, utilizando o comando: 
	- `pytests --pdb`.

# Fazendo reports (resultado de teste em documentos separados)
- O pytest contém uma ferramenta de report padrão, no formato Junit (pedrão dos frameworks de teste). Ou seja, salva em xml.
	- `pytest --junitxml {nome_do_report}.xml`

# Linha de comando
- -v: Mostra o nome dos testes executados.
- -s: Mostra as saidas no console.
- -k {nome_dos_testes}: Filtra resultados.
- -x: Saída rápida.
- `--pdb`: Para debugar quando falhar.

# Marcadores
- Para importar marcadores, basta importar: `from pytest import mark`.
- Tags embutidas em marcadores:
	- @mark.skip: Para pular testes.
	- @mark.skipif: Para pular um teste em determinado contexto.
	- @mark.xfail: É esperado que esse teste falhe em algum contexto.
	- @mark.parametrize: Para parametrizar testes.

## mark parametrize

# References
- https://www.youtube.com/watch?v=MjQCvJmc31A

tags: #programação/python 
status: #zettel/fleeting 
descrição:: Caralho
# O que é venv?
- O python precisa de um ambiente virtual para rodar códigos. Sendo ele local ou global.

- Quando seu projeto não tem uma pasta de venv, ele utilizará o venv global.

- Um ambiente virtual utilizado para guardar instalações de bibliotecas e, rodar se código python.

# Pra que serve?
- O venv guarda todas as versões de bibliotecas, para ver quais bibliotecas você possui naquele determinado ambiente virtual, utilize o seguinte código: `pip freeze`. (Lembrando que o ambiente tem que estar **ativado**, senão ele mostrará o "freeze" do seu python global).

- Então, pra cada projeto você pode ter diferentes ambientes virtuais, com versionamentos de bibliotecas diferentes também.

# Criando uma pasta venv
- Para criar uma venv no seu projeto, basta utilizar o comando: `python -m venv venv`. Sendo o primeiro parâmetro é onde sua venv global está. E o Segundo parâmetro o nome da pasta, geralmente utiliza-se (venv, env, .venv, .env).

# Recriando uma pasta venv através de requirements
- Geralmente, a pasta venv vai ficando pesada, isso pode atrapalhar caso você queira fazer upload/download de um projeto, por isso, usamos requirements.

- Requirements são arquivos .txt que guardan as bibliotecas e suas respectivas versões.

- Para **criar** um requirement, utilize o codigo: `pip freeze > requirements.txt`.
- Para **ativar** um requirement, com o ambiente ativo, utilize o codigo: `pip install -r requirements.txt`.

# Ativando e desativando o venv
- Para **ativar**, é necessário utilizar o seguinte código no seu projeto (windows): `venv\Scripts\activate.bat`.

- Para **desativar**, é necessário utilizar o seguinte código no seu projeto (windows): `deactivate`. 

- Ambiente ativado:
`(venv) C:\Users\luizh\teste_repositorio>`

- Ambiente desativado:
`C:\Users\luizh\teste_repositorio>`

# Estrutura da pasta venv
- A pasta venv é composta por 3 pastas:
	- Include - não sei.
	- Lib - Nesta pasta, você encontra bibliotecas antes intaladas.
	- Scripts - Pasta que carrega os programas executáveis, [[Pip (Preferred Installer Program)]], python, activate etc.

# References
- [Curso de Python do Luiz Otávio Miranda](https://www.udemy.com/user/luiz-otavio-miranda)

tags: #programação/sql  
status: #zettel/fleeting

- Primeiro, checamos se o docker está instalado usando o comando `docker version`.
![[Pasted image 20221219140949.png]]

- Logo após, iremos fazer um download de uma imagem sql.
# O que é uma imagem?
- É um conjunto de arquivos e instruções necessárias para que um container possa rodar.

- Precisamos baixar a imagem sql do docker hub, com o comando `docker pull`.
![[Pasted image 20221219142922.png]]

- Para conferir as imagems que você baixou, use o comando `docker images`.
![[Pasted image 20221219171634.png]]

- Agora você tem que especificar uma dessas três [[Variáveis de ambiente]]:
	- MYSQL_ROOT_PASSWORD (Senha fixa)
	- MYSQL_ALLOW_EMPTY_PASSWORD (senha vazia)
	- MYSQL_RANDOM_ROOT_PASSWORD (gera senha)
- Para passar uma variável de ambiente, você precisa passar o comando com `-e` (environment). Então fica assim: `docker run -e MYSQL_ROOT_PASSWORD=root mysql`.
- Começa a rodar, o problema é, que o terminal trava e é preciso abrir outro.
- Agora você vai passar o mesmo comando com parâmetro adicionais: `docker run -e MYSQL_ROOT_PASSWORD=root --name {nome} -d mysql`.

- Agora, para chegar se está rodando mesmo, use o comando `docker ps`. (se o parâmetro `-a`for adicionado, irá listar os que não estão ativos também).
![[Pasted image 20221219181108.png]]

# Como acessar o servidor
- Apesar do container estar no seu sistema operacional, ele está em uma máquina diferente.
- Então acessamos como um servidor externo, por isso, precisamos saber o endereço (ip) desse servidor.
- Usando o comando docker `inspect {nome}`, irá listar uma série de parâmetros e propriedades especificas da configuração do container.
- Procure o parâmetro "IPAddress", e pronto, ip achado.
![[Pasted image 20221219182822.png]]


# References
- https://www.youtube.com/watch?v=1Zpr1vX0wqk

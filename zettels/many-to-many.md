tags: #programação/sql 
status: #zettel/fleeting

- Não consegue-se fazer esse tipo de relação direto, tem que haver uma "joined-table" entre as tabelas.

![[Pasted image 20221219050924.png]]
- A relação é de muitos para muitos é criada a partir de duas relações de um para muitos ([[one-to-many]]).
- (?) A **PK** da tabela "User_roles" é a composição entre os dois valores (user_id e role_id).
- Isso quer dizer que, eu não posso ter um usuário que tenha um id repitido, com um id de uma role.
Ex:
![[Pasted image 20221219051744.png]]
- Perceba que o útlimo se repitiu no mesmo registro, isso não é permetido.

# References
- [Curso de Python do Luiz Otávio Miranda](https://www.udemy.com/user/luiz-otavio-miranda)
	- Sec. 20 ep. 492.

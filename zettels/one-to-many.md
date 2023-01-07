tags: #programação/sql 
status: #zettel/fleeting

- A ideia é a mesma, uma **PK** de uma tabela na *FK* de outra, o que muda é as quantidades

![[Pasted image 20221219044549.png]]
- Do lado esquerdo, como explicado anteriormente, eu tenho que ter um usuário obrigatoriamente.
- Do direito, está indicanto ===zero ou muitos=== perfis.
- Isso significa que, um usuário pode não ter perfil ou pode ter muitos perfis.

![[Pasted image 20221219045018.png]]
- Neste caso, o usuário continua obrigatório mas tambem torna-se obrigatório ===um ou muitos=== perfis.
- É importante ressaltar que se o usuário tiver um perfil, ele não pode ser apagado, a não ser que quando você peça para apagar o usuário, apague o perfil também. Não é possível ter dados inconsistentes.

# References
- [Curso de Python do Luiz Otávio Miranda](https://www.udemy.com/user/luiz-otavio-miranda)
	- Sec. 20 ep. 491.

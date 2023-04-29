tags: #programação/css 
status: #zettel/fleeting

# Introdução
- CSS (Cascading Style Sheets) — é uma linguagem de folhas de estilos (style sheets) responsável por dar estilo ao [[HTML]]. Essa liga entre HTML e CSS é feita através de seletores css.
```Css
p {
  color: red;
}
```
- Nesse exemplo, seleciona-se todos os parágrafos contidos no HTML e aplica a coloração da fonte destes em vermelho.

## Composição de um conjunto de regras
<img src="https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/CSS_basics/css-declaration-small.png">
- **Seletor (selector)** — é o nome do elemento ou atributo no HTML.
- **Declaração (declaration)** — é a própria regra contendo:
	- **Propriedade (property)** — é a forma pela qual se estiliza o HTML; e
	- **Valor da propriedade (property value)** — escolhe uma de várias aparência contida em uma propriedade.

## Padding, Border e Margin
- São as propriedades mais comuns do css. Torna-se mais fácil se pensarmos em caixas empilhadas, assim que o css funciona.
<img src="https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/CSS_basics/box-model.png">
- **Margin**: espaço extermo de um elemento.
- **Boder**: como o nome diz, a borda ou linha sólida do lado de fora do padding.
- **Padding**: o espaço ao redor do conteúdo.

# Seletores
- Para selecionar uma "class", usa-se (.) e para selecionar um "id", usa-se (#).

# References
- MDN
	- https://developer.mozilla.org/pt-BR/docs/Learn/Getting_started_with_the_web/CSS_basics

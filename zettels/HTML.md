tags: #programação/html 
status: #zettel/fleeting


# Introdução
- HTML é uma linguagem de marcação composta por uma série de elementos que demarcam um certa estrutura.

## Composição de um elemento
<img src="https://developer.mozilla.org/pt-BR/docs/Learn/Getting_started_with_the_web/HTML_basics/gato-rabujento-pequeno.png">
- **Tag**: há dois tipos, de abertura e de fechamento, serve para delimitar o conteúdo. Há exceções que a tag necessita apenas de abertura.
- **Conteúdo**: auto-explicativo. Sem não houver conteúdo é chamado de elemento vazio.
- **Elemento**: é o conjunto desses dois.

### Atributos em elementos
<img src="https://developer.mozilla.org/pt-BR/docs/Learn/Getting_started_with_the_web/HTML_basics/gato-rabujento-atributo-pequeno.png">
- Elementos podem ter atributos que servem para identificar certos elementos para posteriormente aplicar um estilo ou outras coisas.

## Anatomia de um documento HTML
- É permitido o aninhamento de elementos, claro, respeitando a sitaxe das tags.
- Em seguida veremos um documento HTML básico.
```Html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8" />
    <meta name="viewport" content="width=device-width" />
    <title>Minha página de teste</title>
  </head>
  <body>
    <img src="images/firefox-icon.png" alt="minha página de teste">
  </body>
</html>
```
- `<!DOCTYPE html>` — o doctype. É a parte inicial obrigatória do documento. Nas névoas do tempo, quando o HTML era novo (por volta de 1991/2), doctypes eram criados para agir como links para um conjunto de regras que a página HTML tinha que seguir para ser considerada um bom HTML, o que poderia significar checagem automática de erros e outras coisas úteis. No entanto, atualmente, eles não fazem muito sentido e são basicamente necessários apenas para garantir que o documento se comporte corretamente. Isso é tudo que você precisa saber agora.
- `<html>` — elemento que envolve todo o html, conhecido por ser o elemento raiz.
- `<head>` — elemento que não deve haver conteúdo. Usado para recipiente de scripts, estilos etc...
- `<meta charset="utf-8">` — define o conjunto de caracteres que o documento vai usar.
- `<title>` — define o título da página, que é onde aparece no navegador.
- `<body>` — contém todo o conteúdo quer você quer mostrar ao público.
- `<img>` — elemento vazio que deve possuir uma imagem em seu atributo.

## Imagens
- Para adicionar imagens em seu HTML é necessário o elemento vazio `<img>`.
```Html
<img src="images/firefox-icon.png" alt="Minha imagem de teste">
```
- É possível usar dois atributos para contextualizar uma imagem. O "src" que é o caminho da nossa imagem. Já o "alt" serve como uma descrição da imagem, servem se caso o usuário é cego ou se a imagem não carregou.

## Links
- É literalmente onde a internet vira uma rede, sendo assim, essenciais. Usa-se a tag `<a>` junto ao atribudo "href" (**h**ypertext **ref**erence).
```HTML
<a href="https://www.youtube.com/?hl=pt&gl=BR">Youtube</a>
```

- É possível também linkar um [[CSS]], utilizando um elemento vazio com a tag `<link>` e dois atributos "href" e "rel":
```Html
<link href="estilos/estilo.css" rel="stylesheet">
```
- Com a tag `<link>` há também a possibilidade de importar fontes do [Google Fonts](https://fonts.google.com), podendo usar no seu CSS:
```Html
<link href="http://fonts.googleapis.com/css?family=Open+Sans" rel="stylesheet">
```

# Atributos
## Class e Id
- Os dois atributos de identificação são a "class" — que pode ser usada em vários elementos de uma vez e várias classes em um mesmo elemento — e o "id" — que é restrito a um único elemento.
```Html
<!-- class -->
<h1 class="classe1 classe2">...</h1>
<h2 class="classe1">...</h2>

<!-- id -->
<h1 id="id">...</h1>
```

# References
- MDN
	- [Tags HTML](https://developer.mozilla.org/pt-BR/docs/Web/HTML/Element)
	- https://developer.mozilla.org/pt-BR/docs/Learn 💡
	- https://developer.mozilla.org/pt-BR/docs/Learn/Getting_started_with_the_web/HTML_basics
	- https://developer.mozilla.org/pt-BR/docs/Web/Accessibility
- Google
	- https://developers.google.com/search/docs/crawling-indexing/qualify-outbound-links?hl=pt-br
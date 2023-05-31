tags: #programação/javascript #activereacall 

# Livro 1
- Referência: https://github.com/cezaraugusto/You-Dont-Know-JS/tree/portuguese-translation/up%20%26%20going
## 1. Como escrevo "Olá, mundo!" no terminal?
```js
console.log("Olá, mundo!");
```
---
## 2. O que é uma "tipagem forte" e uma "tipagem fraca"?
- Tipagem forte — também conhecida por tipagem estática —, é quando uma variável, quando declarada, terá somente um tipo. Tipagem fraca — também chamada de tipagem dinâmica —, é o contrário, uma variável pode comportar vários tipos diferentes.
---
## 3. O que é e como declarar uma constante?
- Constante é a variável declarada que não pode mudar seu valor.
```js
const constante;
```
---
## 4. Como funcionam as variáveis dessa linguagem?
- Como dito antes, a linguagem é tipagem dinâmica, ou seja, uma variável pode comportar diversos tipos ao decorrer do código. Você pode não declará-las — sem palavras privadas anteriores, com isso, não importa onde declarada, vai ser uma variável global —, ou com uma palavra privada, dentre essas:
	- **var**: declaração referente ao escopo ou, se não houver, global;
	- **let**: declara uma variável local no escopo de bloco; e
	- **const**: que, como dito antes, declara um valor fixo, ou seja, que não se pode alterar.
- Quando declaradas, as variáveis são criadas antes mesmo do código começar — isso é chamado de *"hoisting"*.
---
## 5. Quais os tipos e como descobri-los?
- São chamado tipos primitivos:
	- **Boolean**: true or false;
	- **null**: valor nulo;
	- **undefined**: valor não definido;
	- **Number**: 32 ou 3.1415;
	- **BigInt**: suporta mais que o número inteiro máximo (9007199254740991);
	- **String**: "valor entre aspas";
	- **Symbol**: tipo de dado no qual as instâncias são únicas e imutáveis; e
	- **Object**.
- Para descobrir o tipo de uma variável, basta utilizar a função typeof:
```js
var a = 3;
typeof a; // Number
```
---
## 6. Como funcionam as condicionais dessa linguagem?
### IF
```js
if (a == 2) {
    // faça alguma coisa
}
else if (a == 10) {
    // faça outra coisa
}
else if (a == 42) {
    // faça outra coisa diferente
}
else {
    // resultado se nenhuma instrução for atendida (fallback)
}
```

### Operador condicional (? e :)
```js
var a = 42;

var b = (a > 41) ? "hello" : "world";

// similar a:

// if (a > 41) {
//    b = "hello";
// }
// else {
//    b = "world";
// 
```

### Switch
```js
switch (a) {
    case 2:
    case 10:
        // alguma coisa legal
        break;
    case 42:
        // outra coisa
        break;
    default:
        // resultado se nenhuma instrução for atendida (fallback)
}
```
---
## 7. Como funcionam os loops dessa linguagem?
### for
```js
for (let i = 0; i <= 10; i++) {
    console.log(i);
}
```
- É dividido em dois parâmetros obrigatórios: declaração de variável e limite; e um opicional: o incremento, é possível colocar o incremento dentro do bloco.

### while
- Código executado depois da iteração:
```js
while (numOfCustomers > 0) {
	console.log( "Como posso ajudar?" );
	numOfCustomers = numOfCustomers - 1;
}
```
- E antes da iteração:
```js
do {
	console.log( "Como posso ajudar?" );
	numOfCustomers = numOfCustomers - 1;
} while (numOfCustomers > 0);
```
- Em sua expressão — como condição, aceita parâmetros booleanos.
- A palavra "break;" irá quebrar qualquer um desses loop's, se chamada.
---
## 8. Como funcionam as funções dessa linguagem?
- Como toda linguagem, serve para receber e retornar parâmetros, e também de maneira a reutilizar o código.
```js
function multiply(a, b) {
    return a * b;
}
```
- Caso necessário, consegue-se colocar uma função em uma variável:
```js
var multiplica = function multiply(a, b) {
    return a * b;
}
```
- Cada função possui seu próprio escopo, ou seja, variáveis criadas nela, irão permanecer nela.
- Há também as IIFEs (immediately invoked function expression ou, traduzindo, Expressões de Função Invocadas Imediatamente) que são funções que executam ao serem criadas:
```js
(function IIFE(){
    console.log( "Hello!" );
})();
```
- Uma função cercada de parênteses e com "()" no final, referindo-se a execução da mesma.
---
## 9. O que é uma closure nessa linguagem?
- Acontece quando uma função encapsula outra que espera para ser executada posteriormente.
```js
function makeMultiplyer (x) {

    function multiply (y) {
        return y * x;
    }
    return multiply;
}

double = makeMultiplyer(2);
triple = makeMultiplyer(3);

console.log(double(12)); //24
console.log(triple(12)); //36
```
- Nesse exemplo, o multiplicador é salvo em uma variável e, logo após, é chamado denovo com outro parâmetro.
---
## 10. Qual o iterável que comporta valores em posições enumeradas?
- Um array — que é representado por índice, sempre sendo um número inteiro e, um valor, podendo ser de qualquer tipo, declara-se:
```js
var frutas = ["maçã", "banana"];
```
- Com esse tipo de dado, é possível executar métodos para adicionar, remover, procurar índice, etc. Para iterar um array, faça o seguinte:
```js
frutas.forEach(function (item, indice, array) {
    console.log(item, indice);
}); // Maçã 0 
	// Banana 1
```
---
## 11. Qual o iterável que comporta chave-valor nessa linguagem?
- Na programação chamado de [Vetor associativo](https://pt.wikipedia.org/wiki/Vetor_associativo), é um objeto com chave e valor, declara-se:
```js
objeto = {
    'var1': 'maça',
    'var2': 'banana'
};
```
- Ambos, chave e valor, podem suportar strings, números e variáveis, mas apenas o valor consegue suportar todos os tipos disponíveis.
---
## 12. O que é coerção?
- No javascript, a coerção vem de duas formas: implícita e explícita. A coerção explícita é quando, obviamente, você deixar explícito no código, como por exemplo:
```js
var a = "42";
var b = Number(a);
```
- Coerção implícita:
```js
var a = "42";

var b = a * 1;  // "42" implicitamente coagido para 42 aqui

a;              // "42"
b;              // 42 -- o número!
```
---
## 13. Explique o conceito de "truthy" e "falsy".
- É quando ocorre uma coerção de um valor não-booleano para um booleano.
- Valores "falsy", ou seja, que retornam false:
	- "" (string vazia);
	- 0, -0, NaN (number inválido);
	- null, undefined;
	- false.
- Valores "truthy", ou seja, que retornam true:
	- "hello";
	- 42;
	- true;
	- `[]`, `[1, "2", 3]` (arrays);
	- {}, {a: 42} (objects);
	- function foo () {..} (functions).
## 14. Quais são seus operadores de igualdade?
- São eles: `(==)`, `(===)`, `(!=)` e `(!==)`. Sendo o caractere (!) uma não-igualdade que não deve ser confundido com desigualdade.
- A diferença entre `(==)` e `(===)` é dada pela coerção, ou seja, `(==)` verifica a igualdade com a coerção ativa e `(===)` não. Ex:
```js
var a = "42";
var b = 42;

a == b;         // true
a === b;        // false
```
- A não igualdade comporta-se igualmente sendo `(!=)` para `(==)` e `(!==)` para `(===)`.
---
## 15. Quais são seus comparadores relacionais? Ou seja, operadores de desigualdade.
- São eles: (<), (>), (<=), (>=), maior, menor, maior ou igual e menor ou igual respectivamente.
- É possível comparar strings também, sendo em ordem alfabética.
---

# Livro 2
- Referência: https://github.com/cezaraugusto/You-Dont-Know-JS/tree/portuguese-translation/scope%20%26%20closures
## 1. O que é escopo?
- É o conjunto de regras que determinam onde e como um identificador pode ser buscado. São divididos em dois, escopo global e local. O escopo local pode ser uma função que, variáveis declaradas em seu interior, pertencem somente àquela função. Há também blocos, pode exemplo:
### Bloco de código
```js
{
    var a = 1;
}
console.log(a); // 1
```
### Bloco de função
```js
function myFunction() {
    var a = 1;
}
console.log(a); //ReferenceError
```
### Bloco de condicional
```js
if (true) {
    var a = 1;
}
console.log(a); // 1
```
### Bloco de loop
```js
for (let i; i < 10; i++) {
    var a = 1;
}
console.log(a); //undefined
```
- O resultado é "undefined", porque a busca RHS está acontecendo dentro do bloco for, e como a busca LHS acontece um "hoisting", ela é declarada primeiro, por isso ocorre desta variável estar vazia.
## 2. O que é um compilador e o que, basicamente, ele faz?
- É um programa que traduz linguagem escrita por um humano para uma linguagem de máquina.
## 3. Qual o elenco para fazer um programa javascript rodar?
## 4. O que são referências LHS e RHS?
## 5. o que é escopo léxico?
## 6. O que é "shadowing" ou sombreamento?
## 7. O que é o "Princípio do privilégio mínimo"?
## 8. O que são blocos explícitos e para que servem?
## 9. Quando declarar uma variável let?
## 10. Como importar e exportar um identificador?

# Reference
- https://github.com/cezaraugusto/You-Dont-Know-JS/tree/portuguese-translation
- MDN
	- https://developer.mozilla.org/pt-BR/docs/Learn/Getting_started_with_the_web/JavaScript_basics
	- https://developer.mozilla.org/pt-BR/docs/Web/JavaScript
	- https://developer.mozilla.org/pt-BR/docs/Learn/JavaScript
- https://roadmap.sh/javascript
- https://devdocs.io/javascript/
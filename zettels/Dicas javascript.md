tags: #programação/javascript

- [Colocar input](https://stackoverflow.com/questions/54486307/referenceerror-prompt-is-undefined-how-would-i-fix-this-in-javascript/73105774#73105774)
	- Open terminal and run:-
	- Step 1: `npm init`  
	- Step 2: `npm install prompt-sync`  
	- Step 3: Open the js file (name.js) in which you want to use prompt and `import` the prompt-sync as given below. (on line 1)
	- eg: `const prompt = require("prompt-sync")();`
```javascript
const prompt = require("prompt-sync")();

let a = prompt("enter a number: ");
console.log(a);
```
- Expressões são declaradas dentro delas mesmas, não afetando o escopo externo.

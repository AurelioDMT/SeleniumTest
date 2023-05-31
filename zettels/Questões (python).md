tags: #programação/python #activereacall 
status: #zettel/fleeting

# Módulos diversos
1. 

# Tkinter and ttk
- Referência
	- [The ultimate introduction to modern GUIs in Python ( with tkinter )](https://youtu.be/mop6g-c5HEY)
	- [tkinter doc](https://docs.python.org/pt-br/3/library/tkinter.html#)
	- [ttk doc](https://docs.python.org/pt-br/3/library/tkinter.ttk.html#)
## 1. Como faço para uma janela rodar?
- Esse é o começo, o código básico que faz qualquer janela rodar:
```Python
import tkinter as tk
from tkinter import ttk

# criar janela
window = tk.Tk()

# rodar janela
window.mainloop()
```

## 2. O que é um widget?
- Um widget é tudo aquilo que é mostrado na janela. Pode ser uma label, um caixa de texto, um input, um botão etc.

## 3. Como faço para colocar widgets na minha janela?
- Toda widget tem quer ter uma master como referência. Para colocar o widget no layout, é necessário utilizar o método pack():
```Python
widget = ttk.Label(master=window)
widget.pack()
```

## 4. Como eu atribuo uma função em um botão?
- Com o atributo command:
```Python
button = ttk.Button(master=window, command=lambda: print('hello'))
```

## 5. Como posso pegar e setar dados em widgets?
- Para pegar um dado, basta utiliziar o método get() e, para setar um dado, basta utilizar o método configure() ou setar direto como um dicionário:
```Python
# configure
label.configure(text='other text')

# direto
label['text'] = 'other text'
```

## 6. Como posso juntar vários widgets com uma variável só? Ou seja, os widgets tem que compartilhar os mesmos dados.
- Nesse módulo (tk), é permitido usar variáveis que podem pertencer a diversos widgets. Tem variável para cada tipo: string, int, boolean(bool), doble(float).
```Python
import tkinter as tk

string = tk.StringVar()
integer = tk.IntVar()
_float = tk.DoubleVar()
boolean = tk.BooleanVar()
```
- Essas variáveis são atribuidas em widgets através dos parâmetros nomeados "textvariable" para texto e "variable" para os outros.
```Python
# tkinter variable
string_var = tk.StringVar(value='start value')

# widgets
label = ttk.Label(master=window, text='label', textvariable=string_var)
label.pack()

entry = ttk.Entry(master=window, textvariable=string_var)
entry.pack()
```
- Nesse exemplo eu linkei 2 widgets para ter o mesmo texto.

## 7. Quais são os três tipos de botão?
- Há 3 tipos de botões com características diferentes:
	- Button — botão normal.
	- Checkbutton — botão estilo *checkbox*, ou seja, ativo ou não.
	- Radiobutton — botão que compartilha o estado com outros do mesmo tipo, ou seja, somente um radio, mantendo as características normais, pode estar ativo, se o parâmetro "value" for diferente.
- (EXERCÍCIO) Crie um checkbutton e dois radiobottuns:
	- Checkbutton: apertar o botão printa o valor do radiobutton.
	- Radiobuttons: valores são A e B respectivamente; Clincando em qualquer um, deve printar o valor do checkbutton; e dar uncheck no checkbutton.
	- Use variáveis booleanas!!

## 8. O que é e como funciona um evento?
- Referência
	-  https://www.pythontutorial.net/tkinter/tkinter-event-binding/
```php
eventos podem ser várias coisas:
	input do teclado;
	widgets mudando;
	widgets sendo selecionados/desselecionados;
	click do mouse/movimento/rodinha do mouse.

esses eventos podem ser observados e utilizados.
	Por exemplo, executar uma função quando um botão for pressionado.

você precisa vincular eventos em um widgets com Widget.blind(event, function)

format: modifier-type-detail
	E.g.: Alt-Keypress-a
```
- (EXERCÍCIO) Crie um evento que printe 'Mousewheel' quando o usuário precionar `shift + mousewheel`.

# References
- [Curso de Python do Luiz Otávio Miranda](https://www.udemy.com/user/luiz-otavio-miranda)

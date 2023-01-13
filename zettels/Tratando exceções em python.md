tags: #programação/python 
status: #zettel/fleeting

# O que são exceções em python?
- São classes, executando quando um determinado erro é executado em seu código. Classe principal que engloba todos os erros, ou seja, todos os erros *herdam* dela.

# Tratamento
- Usa-se as seguintes palavras privadas:
	- try. - espaço para ocorrer algum erro.
	- except. - espaço para capturar esse erro. O código no "try" é pausado.
	- finally. - espaço onde sempre será executado um código.
	- else. - espaço executado apenas se o código execute sem erros.

## Instânciando a classe Except
- Da pra instânciar a classe de um erro atravez do "except":
```Python
try:
    print(None / 2)
except Exception as error:
    # Nome da class
    print(error.__class__.__name__)
-----------------------------------------
TypeError
```

- Caso souber o nome da classe, coloque-a no lugar do "Exception".
```Python
try:
    print(None / 2)
except TypeError as error:
    print(error)
-----------------------------
unsupported operand type(s) for /: 'NoneType' and 'int'
```

## Hierarquia das exções
BaseException
 ├── BaseExceptionGroup
 ├── GeneratorExit
 ├── KeyboardInterrupt
 ├── SystemExit
 └── Exception
      ├── ArithmeticError
      │    ├── FloatingPointError
      │    ├── OverflowError
      │    └── ZeroDivisionError
      ├── AssertionError
      ├── AttributeError
      ├── BufferError
      ├── EOFError
      ├── ExceptionGroup
      ├── ImportError
      │    └── ModuleNotFoundError
      ├── LookupError
      │    ├── IndexError
      │    └── KeyError
      ├── MemoryError
      ├── NameError
      │    └── UnboundLocalError
      ├── OSError
      │    ├── BlockingIOError
      │    ├── ChildProcessError
      │    ├── ConnectionError
      │    │    ├── BrokenPipeError
      │    │    ├── ConnectionAbortedError
      │    │    ├── ConnectionRefusedError
      │    │    └── ConnectionResetError
      │    ├── FileExistsError
      │    ├── FileNotFoundError
      │    ├── InterruptedError
      │    ├── IsADirectoryError
      │    ├── NotADirectoryError
      │    ├── PermissionError
      │    ├── ProcessLookupError
      │    └── TimeoutError
      ├── ReferenceError
      ├── RuntimeError
      │    ├── NotImplementedError
      │    └── RecursionError
      ├── StopAsyncIteration
      ├── StopIteration
      ├── SyntaxError
      │    └── IndentationError
      │         └── TabError
      ├── SystemError
      ├── TypeError
      ├── ValueError
      │    └── UnicodeError
      │         ├── UnicodeDecodeError
      │         ├── UnicodeEncodeError
      │         └── UnicodeTranslateError
      └── Warning
           ├── BytesWarning
           ├── DeprecationWarning
           ├── EncodingWarning
           ├── FutureWarning
           ├── ImportWarning
           ├── PendingDeprecationWarning
           ├── ResourceWarning
           ├── RuntimeWarning
           ├── SyntaxWarning
           ├── UnicodeWarning
           └── UserWarning

# References
- 

tags: #programação/python/biblioteca 
Doc: https://pypi.org/project/python-dotenv/

- Para usar [[Variáveis de ambiente]] em python, é necessário instalar a biblioteca "python-dotenv". `pip install python-dotenv`.

- **É NECESSÁRIO** criar um arquivo ".env" na raiz do seu projeto, para armazenar as variáveis de ambiente. ==E geralmente, não vai para nenhum repositório== (gitignore).
	- https://github.com/github/gitignore/blob/main/Python.gitignore

- As variáveis de ambiente são valores que podem ser usados em seu código e que podem variar dependendo do ambiente em que o seu código está sendo executado (por exemplo, o ambiente de produção ou o ambiente de desenvolvimento).

- Esse arquivo deve conter as suas variáveis de ambiente e seguir o seguinte formato:
	- VARIAVEL_DE_AMBIENTE_1=valor
	- VARIAVEL_DE_AMBIENTE_2=valor
	- VARIAVEL_DE_AMBIENTE_3=valor

# Salvando variáveis de ambiente
- Depois de criado sua ".env" e colocado suas variáveis, para oficializar isso no código, basta:
```Python
from dotenv import load_dotenv  # type: ignore

load_dotenv()
```

# Obtendo variáveis de ambiente
- Depois de carregar suas variáveis, para obtê-las usa-se o módulo OS ([[OS em python]]):
```Python
print(os.getenv('BD_PASSWORD'))
print(os.environ['BD_PASSWORD'])
```
- No caso do dicionário, você pode também criar variáveis atribuindo valor e chave.
- `os.environ['BD_PASSWORD'] = 1234`

# Reference
- [Curso de Python do Luiz Otávio Miranda](https://www.udemy.com/user/luiz-otavio-miranda)
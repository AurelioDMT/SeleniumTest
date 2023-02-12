tags: #programação/python/code  

- Código do curso. Criar um log para ser utilizado por outras classes.

# Path
📂Mixins	
├── 📂log.py
└── 📂eletronico.py 

# log.py
```Python
from pathlib import Path

LOG_FILE = Path(__file__).parent / 'log.txt'


class Log:
    def _log(self, msg):
        raise NotImplementedError('implemente o método log')
    
    def log_error(self, msg):
        return self._log(f'Error: {msg}')

    def log_success(self, msg):
        return self._log(f'Success: {msg}')

class LogFileMixin(Log):
    def _log(self, msg):
        print(msg)
        format_msg = f'{msg} ({self.__class__.__name__})'
        with open(LOG_FILE, 'a', encoding='utf8') as file:
            file.write(format_msg)
            file.write('\n') 

class LogPrintMixin(Log):
    def _log(self, msg):
        print(f'{msg} ({self.__class__.__name__})')


if __name__ == '__main__':
    l = LogFileMixin()
    l.log_error('suicideboys')
    l.log_success('antontio')
```
- Importamos a classe "Path" para pegar o caminho atual do arquivo, para contatenar com o arquivo que iremos criar.

- A classe "Log", é um exemplo básico de abstração. Ou seja, ela não está ali para ser utilizada diretamente, mas sim, por outras classes.

- Nesse código, reescrevemos apenas o métodod "`_log`". Os outros métodos retornam ele, então, é por isso.

- Implementamos a função "`_log`" diferente nas duas classes. Na classe "LogPrintMixin" apenas imprimimos o log, já na classe "LogFileMixin", imprimimos e salvamos em um arquivo txt.

# eletronico.py
```Python
from log import LogFileMixin


class Eletronico:
    def __init__(self, nome) -> None:
        self.nome = nome
        self._state = False
    
    def ligar(self):
        if not self._state:
            self._state = True
        
    def desligar(self):
        if self._state:
            self._state = False
    

class Smartphone(Eletronico, LogFileMixin):
    def ligar(self):
        super().ligar()

        if self._state:
            msg = f'{self.nome} está ligado.'
            self.log_success(msg)


    def desligar(self):
        super().desligar()

        if not self._state:
            msg = f'{self.nome} está desligado.'
            self.log_success(msg)


iphone = Smartphone('iphone')
iphone.ligar()
iphone.desligar()
```
- Código basico que, tem uma classe pai chamada "Eletronico" que tem os métodos liga e desliga.
- Classe filha "Smartphone" que herda de "Eletronico" e "LogFileMixin", liga e desliga e manda pro log.

# Reference
- [Curso de Python do Luiz Otávio Miranda](https://www.udemy.com/user/luiz-otavio-miranda)
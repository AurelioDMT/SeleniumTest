tags: #programação/python/funções 

# Definição e uso
- A função "open()" abre um arquivo e retorna ele como um file object.

# Sintaxe
- `open(file, mode)`

## Valor dos parâmetros
| Parâmetro | Descrição |
| - | - |
| file | O caminho e o nome do arquivo.
| mode | Uma string que define qual modo abrirá o arquivo.
| | "r" - Ler - Valor padrão. Abre o arquivo para ler. Erro se o arquivo não existir.
| | "a" - Adicionar - Abre o arquivo para escrever ao final (não apaga o que está escrito). Cria o arquivo se não existir.
| | "w" - Escrever - Abre o arquivo para escrever (apaga o que está escrito). Cria o arquivo se não existir.
| | "x" - Criar - Cria um arquivo específico. Retorna um erro se o arquivo já existir.
| | "+" - Ler e escrever.
| | Você pode escolher se vai salvar em texto ou binário.
| | "t" - Texto - Valor padrão.
| | "b" - Binário.

# Reference
- https://www.w3schools.com/python/ref_func_open.asp
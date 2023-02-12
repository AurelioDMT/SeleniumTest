tags: #programação/python/code 

```Python
import os
import shutil

HOME = os.path.expanduser('~')
PICTURES = os.path.join(HOME, 'Pictures')
PASTA_ORIGINAL = os.path.join(PICTURES, 'ai_images')
NOVA_PASTA = os.path.join(PICTURES, 'cópia_ai_images')

# shutil.rmtree(NOVA_PASTA, ignore_errors=True)
shutil.copytree(PASTA_ORIGINAL, NOVA_PASTA)
```
- Você pode simplificar o código ([[Copiando arquivos de um diretório para outro (um por um)]]), mas ai você não um controle total.
- Bascicamente, declaramos as constantes e damos um =="shutil.rmtree" para remover uma pasta recursivamente== ou "shutil.copytree" para copiar a pasta e todas as suas subpastas.

# Reference
- [Curso de Python do Luiz Otávio Miranda](https://www.udemy.com/user/luiz-otavio-miranda)
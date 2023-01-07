tags: #programação/python 

```python
def criar_multiplicador(multiplicador):
    def multiplicar(numero):
        return numero * multiplicador
    return multiplicar
  

duplicar = criar_multiplicador(2)
triplicar = criar_multiplicador(3)
quadriplicar = criar_multiplicador(4)

print(duplicar(4))
print(triplicar(4))
print(quadriplicar(4))
```

# Reference
- 
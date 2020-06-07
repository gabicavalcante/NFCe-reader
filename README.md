# nfce reader

Esse projeto foi feito pra faciliar as compras :) O Notebook lê as Notas Fiscais do Consumidor Eletrônica (NFC-e) e organizar os itens comprados em um dataframe, adicionando o dia da semana em que eles foram comprados.

Basta definir uma lista de dicionário com as seguintes infos:
```python
nfs = [
    {
        "date": "2020-06-06",
        "local": "supermercado X",
        "url": "http://nfce.set.rn.gov.br/c..."
    },
    {
        "date": "2020-05-31",
        "local": "supermercado Y",
        "url": "http://nfce.set.rn.gov.br/p.."
    },
    ...
   }
]
```

Esses dicionários são definidos na primeira célula do notebook, preencha com os seus dados. No meu caso, minha nota fiscal é feita pelo governo do RN, dependendo de onde você more, talvez a estrutura mude. Mas não deve ser complicado adaptar. A biblioteca usada no projeto para extrair os dados é a [`rows`](https://github.com/turicas/rows), talvez no seu caso baste mudar o atributo `index` na chamada `rows.import_from_html`, esse argumento informa qual é a *table* que você quer pegar. 

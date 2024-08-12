# Descobrindo-quais-as-franquias-que-t-m-maior-n-mero-de-funcion-rios
Descobrindo quais as franquias que têm maior número de funcionários

### Você trabalha em uma empresa que possui várias franquias. Queremos saber quais as franquias que têm maior número de funcionários e quais dessas, juntas, representam 80% dos funcionários da rede toda.
franquias = [
    (25000, "Loja A"),
    (10000, "Loja B"),
    (500, "Loja C"),
    (25000, "Loja D"),
    (1200, "Loja E"),
    (400, "Loja F"),
    (200, "Loja G"),
    (15, "Loja H"),
    (200, "Loja I"),
    (15, "Loja J"),
    (200, "Loja K"),
    (15, "Loja L"),
    (200, "Loja M"),
    (15, "Loja N"),
]

franquias.sort(reverse=True)
total_funcionarios = sum(item[0] for item in franquias)

percentual_acumulado = 0

for i in range(len(franquias)):
    qtde_funcionarios, descricao = franquias[i]
    percentual_acumulado += qtde_funcionarios / total_funcionarios
    franquias[i] = (qtde_funcionarios, descricao, qtde_funcionarios / total_funcionarios, percentual_acumulado)

print(franquias)

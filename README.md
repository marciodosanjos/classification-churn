# classification-churn

Projeto de análise e classificação para prever quais linhas têm maior probabilidade de churn no mês seguinte, apoiando a priorização de ações de retenção de clientes.

## Definição de churn

Churn é a saída de uma linha por cancelamento ou portabilidade.

A taxa mensal é calculada como:

Taxa de churn (%) = (linhas perdidas no período / total de linhas elegíveis no início do período) × 100

A unidade de análise é a linha, pois um cliente pode possuir mais de uma.

## Janela de observação

O modelo será executado uma vez por mês, utilizando apenas informações disponíveis até a `data_corte` para prever churn no mês seguinte.

Exemplo: a base de 31/10 será utilizada para prever as saídas de novembro.

## Variável target

Target variable: `churn_vol_30d`:

- `0`: a linha não saiu no mês seguinte.
- `1`: a linha saiu por cancelamento ou portabilidade no mês seguinte.

Apesar do nome `30d`, a definição da target considera o mês seguinte.

## Etapa atual

- Load dataset.
- Checking dimensions, types, null values and duplicates.
- Analysis of the target distribution.
- Calculation of the churn rate for the reference month.

## Ferramentas

- Python 3.12
- pandas
- Jupyter Notebook
- Visual Studio Code

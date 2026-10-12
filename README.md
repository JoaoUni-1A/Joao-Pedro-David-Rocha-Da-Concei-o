# Experiência Prática I: Inteligência Artificial e Programação para Engenharia

Este repositório contém o conjunto de dados e a documentação inicial para o desenvolvimento de um sistema de monitoramento e manutenção preditiva industrial, conectando conceitos teóricos de engenharia, ciência de dados e inteligência artificial.

## 1. Caracterização do Conjunto de Dados Selecionado

O conjunto de dados escolhido para guiar este projeto é o **AI4I 2020 Predictive Maintenance Dataset**, um banco de dados que reflete o comportamento operacional real e os padrões de falha de maquinários em uma linha de produção.

* **Domínio de Engenharia:** Automação Industrial e Engenharia de Manutenção (Monitoramento de Condição / *Condition Monitoring*).
* **Dimensões Físicas:** O arquivo conta com exatamente **10.000 registros (linhas)**, onde cada linha representa um minuto de operação do equipamento.
* **Formato de Estruturação:** Arquivo **CSV (Valores Separados por Vírgula)** com cabeçalhos claros na primeira linha, sem células mescladas ou anotações flutuantes, ideal para importação direta via Python (Pandas).
* **Fonte Original:** [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/601/ai4i+2020+predictive+maintenance+dataset)

---

## 2. Dicionário de Variáveis (Metadados)

Para garantir a rastreabilidade e a confiabilidade das análises, as variáveis do arquivo foram mapeadas tecnicamente conforme a tabela abaixo:

| Nome Exato da Coluna | Tipo de Dado Esperado | Significado e Unidade de Medida |
| :--- | :--- | :--- |
| `UDI` | Numérico (Inteiro) | Identificador único e sequencial do registro (de 1 a 10.000). |
| `Product ID` | Texto (String) | Código do produto. A letra inicial (L, M ou H) indica a classe de qualidade do equipamento. |
| `Air temperature [K]` | Numérico (Decimal) | Temperatura do ar ambiente medida em Kelvin (K). Monitora as condições térmicas externas. |
| `Process temperature [K]` | Numérico (Decimal) | Temperatura gerada pela operação de fabricação em Kelvin (K). Indica o aquecimento interno do processo. |
| `Rotational speed [rpm]` | Numérico (Inteiro) | Velocidade de rotação do eixo do motor em Rotações por Minuto (rpm). |
| `Torque [Nm]` | Numérico (Decimal) | Força de torção mecânica exercida pela máquina medida em Newton-metro (Nm). |
| `Tool wear [min]` | Numérico (Inteiro) | Tempo acumulado de uso e desgaste da ferramenta de corte em minutos (min). |
| `Machine failure` | Numérico (Binário) | Indicador de quebra do equipamento (Sem unidade). Sendo 0 para operação normal e 1 para falha. |

> **Nota sobre falhas específicas:** O conjunto também traz colunas binárias adicionais detalhando a causa exata da pane (se houver): `TWF` (Desgaste da ferramenta), `HDF` (Dissipação térmica), `PWF` (Falha de potência), `OSF` (Sobrecarga física) e `RNF` (Falhas aleatórias).

---

## 3. Como Carregar os Dados no Python

Você pode carregar este conjunto de dados diretamente em seu script utilizando o código padrão abaixo:

```python
import pandas as pd

# Link de download direto do arquivo hospedado
url = "https://github.com/CleitonM/datasets/raw/main/ai4i2020.csv"

# Carregando os dados com Pandas
df = pd.read_csv(url)

# Visualizando as primeiras linhas do projeto
print("Dados carregados com sucesso!")
print(df.head())
```

---

## 4. Instruções de Postagem no GitHub

Para que o seu trabalho seja avaliado com sucesso pelo professor:
1. Crie um repositório público no seu perfil do GitHub (ex: `experiencia-pratica-ia-engenharia`).
2. Salve este conteúdo em um arquivo chamado `README.md` na raiz do seu repositório.
3. Adicione o seu script Python ou Notebook Jupyter no mesmo local.
4. Garanta que o link do seu repositório esteja público para que a banca possa validar a sua entrega.
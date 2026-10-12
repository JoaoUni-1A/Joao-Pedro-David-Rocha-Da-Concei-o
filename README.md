# Experiência Prática I - Inteligência Artificial e Programação para Engenharia

Este repositório contém o conjunto de dados estruturado e a documentação inicial para o projeto de monitoramento de condições operacionais e manutenção preditiva em ambiente industrial.

## 📊 Caracterização do Conjunto de Dados Selecionado

*   **Domínio de Engenharia:** Automação Industrial e Engenharia de Manutenção (Monitoramento de Condições / *Condition Monitoring*).
*   **Dimensões Físicas:** 10.000 registros (linhas), onde cada linha representa a amostragem de sensores a cada minuto de operação.
*   **Formato de Estruturação:** Arquivo limpo no formato **CSV**, utilizando a vírgula (`,`) como delimitador padrão, com cabeçalhos na primeira linha e sem células mescladas.

## 📋 Dicionário de Variáveis (Metadados)

| Nome da Coluna | Natureza Computacional | Significado Físico e Unidade de Medida |
| :--- | :--- | :--- |
| `UDI` | Numérico (Inteiro) | Identificador único do registro (ID sequencial de 1 a 10.000). |
| `Product ID` | Texto (String) | Código de identificação do produto (Sufixo L, M ou H baseado na qualidade). |
| `Air temperature [K]` | Numérico (Decimal) | Temperatura do ar ambiente medida pelo sensor em Kelvin (K). |
| `Process temperature [K]` | Numérico (Decimal) | Temperatura interna do processo de fabricação em Kelvin (K). |
| `Rotational speed [rpm]` | Numérico (Inteiro) | Velocidade angular de rotação do motor em Rotações por Minuto (rpm). |
| `Torque [Nm]` | Numérico (Decimal) | Força de torção mecânica exercida pela máquina em Newton-metro (Nm). |
| `Tool wear [min]` | Numérico (Inteiro) | Tempo acumulado de desgaste da ferramenta de corte em minutos (min). |
| `Machine failure` | Numérico (Binário) | Indicador de quebra do equipamento (0 = Operação Normal, 1 = Falha). |

## 🚀 Como Importar no Python (Pandas)

```python
import pandas as pd

# Substitua pela URL do seu arquivo raw do GitHub após fazer o upload
url = "manutencao_preditiva.csv" 
df = pd.read_csv(url)

print("Dados carregados com sucesso!")
print(df.head())
```
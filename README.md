# An-lise_Detalhada_Ro
README - Análise Demográfica de Nascimentos (SINASC_RO_2019)
1. Importando Bibliotecas <a name="import"></a>
python
Copy code
import numpy as np
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt

%matplotlib inline
2. Carregando o DataFrame SINASC <a name="read"></a>
python
Copy code
sinasc_raw = pd.read_csv('SINASC_RO_2019.csv')
sinasc_raw.head()
3. Limpeza e Preparação dos Dados
Certifique-se de que as colunas de idade da mãe e do pai são do tipo numérico.

python
Copy code
sinasc_raw['IDADEMAE'] = pd.to_numeric(sinasc_raw['IDADEMAE'], errors='coerce')
sinasc_raw['IDADEPAI'] = pd.to_numeric(sinasc_raw['IDADEPAI'], errors='coerce')
Tarefa 1
1. Idade média das mães e dos pais por município (coluna munResNome)
python
Copy code
idade_media_mae_pai = sinasc_raw.groupby('munResNome')['IDADEMAE', 'IDADEPAI'].mean().round()
print(idade_media_mae_pai.head())
Tarefa 2
2. Peso médio dos bebês por sexo que nasceram no dia do seu aniversário por faixas de escolaridade da mãe
python
Copy code
# Substitua '10/01' pela data do seu aniversário no formato MM/DD
data_aniversario = '10/01'

# Filtragem para bebês nascidos no dia do aniversário
bebês_aniversário = sinasc_raw[sinasc_raw['DTNASC'].dt.strftime('%m/%d') == data_aniversario]

# Calcule o peso médio dos bebês por sexo e faixa de escolaridade da mãe
peso_medio_por_sexo_escolaridade = bebês_aniversário.groupby(['SEXO', 'ESCMAE'])['PESO'].mean().round(2)
print(peso_medio_por_sexo_escolaridade)
Tarefa 3
3. Qual o município que nasceu menos bebê em 2019?
python
Copy code
# Filtragem para nascimentos em 2019
nascimentos_2019 = sinasc_raw[sinasc_raw['ANO_NASCIMENTO'] == 2019]

# Encontre o município com o menor número de nascimentos
municipio_menos_nascimentos = nascimentos_2019['munResNome'].value_counts().idxmin()

# Estatísticas de idade para mães e pais no município com menos nascimentos
dados_municipio_menos_nascimentos = nascimentos_2019[nascimentos_2019['munResNome'] == municipio_menos_nascimentos]
# ...

# Exiba os resultados
print(f"Município com menos nascimentos em 2019: {municipio_menos_nascimentos}")
# ...
Tarefa 4
4. Qual o município que nasceu mais bebê no mês de março?
python
Copy code
# Filtragem para nascimentos em março
nascimentos_marco = sinasc_raw[sinasc_raw['MES_NASCIMENTO'] == 3]
municipio_mais_nascimentos_marco = nascimentos_marco['munResNome'].value_counts().idxmax()
# ...

# Estatísticas adicionais para o município com mais nascimentos em março
dados_municipio_mais_nascimentos_marco = nascimentos_marco[nascimentos_marco['munResNome'] == municipio_mais_nascimentos_marco]
# ...

# Exiba os resultados
print(f"Município com mais nascimentos em março: {municipio_mais_nascimentos_marco}")
# ...
Análise Detalhada da Demografia de Nascimentos em 2019
python
Copy code
# 1. Distribuição da Idade das Mães e dos Pais:
# ...

# 2. Mapa de Calor das Idades por Município:
# ...

# 3. Gráfico de Barras para Peso Médio por Sexo e Escolaridade:
# ...

# 4. Gráfico para Distribuição de Nascimentos em Março:
# ...

# Influência na Saúde Materna e Infantil:
# ...

# Correlações com Fatores Socioeconômicos:
# ...
Observação: Certifique-se de substituir os comentários por análises específicas e insights derivados dos gráficos e códigos apresentados. Personalize de acordo com os resultados encontrados e os objetivos da análise.







# Análise de Dados do SINASC (Sistema de Informações sobre Nascidos Vivos)
Este projeto visa analisar os dados do SINASC relacionados aos nascimentos ocorridos em 2019. O conjunto de dados utilizado é proveniente do estado de Rondônia (SINASC_RO_2019.csv). A análise é dividida em várias tarefas, cada uma abordando questões específicas relacionadas aos nascimentos, idades dos pais e outros fatores.

## Tarefas Realizadas:
### 1. Idade média das mães e dos pais por município
Limpeza e preparação dos dados, garantindo que as colunas de idade da mãe e do pai sejam do tipo numérico.
Agregação e agrupamento dos dados para calcular a idade média das mães e dos pais por município.
### 2. Peso médio dos bebês por sexo que nasceram no dia do seu aniversário por faixas de escolaridade da mãe
Filtragem dos dados para o dia de aniversário (substituir '10/01' pela sua data de aniversário no formato MM/DD).
Agregação e agrupamento dos dados para calcular o peso médio dos bebês por sexo e faixa de escolaridade da mãe.
### 3. Município que teve o menor número de nascimentos em 2019
Encontrar o município com o menor número de nascimentos.
Estatísticas de idade para mães e pais nesse município.
### 4. Município que teve o maior número de nascimentos no mês de março
Encontrar o município com o maior número de nascimentos no mês de março.
Estatísticas de quantidade de filhos vivos e idade dos pais nesse município.
## Análise Detalhada:
Exploração da distribuição da idade das mães e dos pais.
Mapa de calor mostrando as idades médias por município.
Gráfico de barras para o peso médio dos bebês por sexo e escolaridade da mãe.
Gráfico de barras para a distribuição de nascimentos em março por município.
## Correlações:
Correlação entre idade das mães e peso dos bebês.
Correlação entre idade do pai e peso dos bebês.
## Insights Adicionais:
Detalhes sobre a distribuição de idades das mães e pais.
Visualizações para destacar correlações e padrões.
## Instruções para Replicação:
Bibliotecas Necessárias:

Certifique-se de ter as bibliotecas necessárias instaladas. Você pode instalá-las usando pip install numpy pandas seaborn matplotlib.
Carregando os Dados:

Certifique-se de ter o arquivo 'SINASC_RO_2019.csv' no mesmo diretório do seu script/notebook.
O comando pd.read_csv('SINASC_RO_2019.csv') é usado para carregar os dados. Ajuste o nome do arquivo conforme necessário.
## Execução das Tarefas:

Execute cada célula sequencialmente para realizar as tarefas propostas.
## Personalização:

Substitua a data de aniversário no formato MM/DD para obter resultados personalizados.
Análise Detalhada e Correlações:

A análise detalhada e as correlações fornecem insights adicionais. Personalize conforme necessário.
Visualizações Interativas:

Explore os gráficos interativos para compreender melhor os padrões nos dados.


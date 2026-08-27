# Análise de viagens de táxi em Chicago

Projeto desenvolvido durante o **Sprint 7 do Bootcamp de Ciência de Dados da TripleTen**, utilizando Python, pandas, Matplotlib, Seaborn e SciPy.

## Sobre o projeto

Este projeto analisa viagens de táxi em Chicago com foco na etapa de análise exploratória de dados e no teste de uma hipótese operacional. O estudo utiliza resultados de consultas SQL e investiga quais empresas concentram mais corridas, quais bairros aparecem com maior frequência como destino e se as condições meteorológicas influenciam a duração das viagens entre o Loop e o Aeroporto Internacional O'Hare.

O objetivo é transformar os dados em informações úteis para compreender a demanda de transporte e avaliar se viagens realizadas em sábados chuvosos apresentam comportamento diferente das viagens realizadas em outras condições de sábado.

## Objetivos

O projeto foi desenvolvido para:

- importar e inspecionar os resultados das consultas SQL;
- verificar dimensões, tipos de dados, valores ausentes e estatísticas descritivas;
- identificar as dez principais empresas de táxi por número de corridas;
- identificar os dez principais bairros de Chicago por número médio de viagens finalizadas;
- construir gráficos de empresas e bairros para facilitar a interpretação dos resultados;
- separar as viagens do Loop para O'Hare conforme as condições meteorológicas;
- testar a hipótese sobre a duração média das viagens em sábados chuvosos;
- explicar as hipóteses nula e alternativa, o nível de significância e o critério de decisão.

## Dados utilizados

O notebook utiliza três arquivos de resultados fornecidos pelo projeto:

| Arquivo | Conteúdo |
|---|---|
| `project_sql_result_01.csv` | Número de corridas por empresa de táxi nos dias 15 e 16 de novembro de 2017 |
| `project_sql_result_04.csv` | Bairros de Chicago e número médio de viagens que terminaram em cada bairro em novembro de 2017 |
| `project_sql_result_07.csv` | Data e hora de início, condições meteorológicas e duração das viagens do Loop para O'Hare |

**Os datasets não estão incluídos neste repositório.** Eles devem ser disponibilizados separadamente no diretório `/datasets/`, conforme as instruções originais do curso.

## Etapas desenvolvidas

### 1. Análise exploratória

Os dois primeiros arquivos são carregados e avaliados quanto a formato, tipos de dados, valores ausentes e estatísticas descritivas. O notebook então ordena as empresas por quantidade de corridas e os bairros por número médio de destinos.

### 2. Visualizações

São construídos gráficos de barras para mostrar as empresas de táxi com maior volume de corridas e os dez bairros com maior número médio de viagens finalizadas. As visualizações permitem identificar concentração de demanda e regiões com maior fluxo de desembarque.

### 3. Teste de hipótese

O terceiro arquivo é utilizado para comparar a duração das viagens do Loop para O'Hare em sábados chuvosos e em sábados com outras condições meteorológicas. O teste estatístico é realizado com amostras independentes, nível de significância definido no notebook e interpretação baseada no p-valor.

A formulação adotada é:

- **Hipótese nula (H₀):** a duração média das viagens em sábados chuvosos é igual à duração média das viagens em sábados não chuvosos;
- **Hipótese alternativa (H₁):** a duração média das viagens em sábados chuvosos é diferente da duração média das viagens em sábados não chuvosos.

O critério de decisão é rejeitar H₀ quando o p-valor for menor que o nível de significância escolhido. A justificativa do teste e a conclusão estão registradas no notebook.

## Principais resultados

A análise mostra forte concentração de corridas em um grupo reduzido de empresas, com destaque para a Flash Cab. Entre os destinos, o Loop lidera com ampla vantagem, seguido por River North, Streeterville e West Loop, o que confirma a importância do centro de Chicago como área de chegada.

O teste estatístico avalia se a chuva altera a duração das viagens entre o Loop e O'Hare. A conclusão do notebook é baseada no resultado observado no p-valor e deve ser interpretada especificamente para o conjunto de sábados analisado, sem generalização automática para todos os dias ou trajetos.

## Resultado

O resultado é um diagnóstico de demanda de táxis em Chicago com ranking de empresas, ranking dos dez principais bairros de destino e teste da hipótese sobre a duração de viagens do Loop para O’Hare em sábados chuvosos. As visualizações evidenciam a concentração do fluxo no Loop e em outros bairros centrais, enquanto a conclusão estatística deve ser lida de acordo com o p-valor e o nível de significância registrados no notebook.

## O que aprendi

O projeto consolidou a conexão entre resultados de consultas SQL e análise em Python, incluindo recortes, agrupamentos, ordenação, construção de gráficos e formulação de hipóteses nula e alternativa. Também reforçou a interpretação correta de p-valor, alfa e limitações de generalização.

## Melhorias possíveis

Como evolução, seria possível documentar as consultas SQL originais, apresentar intervalos de confiança e tamanho de efeito, comparar também dias úteis e horários de pico e usar testes robustos ou não paramétricos como análise de sensibilidade. A inclusão de precipitação quantitativa e tempo de deslocamento permitiria uma investigação operacional mais detalhada.

## Tecnologias utilizadas

- Python 3
- pandas
- NumPy
- Matplotlib
- Seaborn
- SciPy
- Jupyter Notebook
- SQL e GitHub

## Como executar

Clone o repositório:

```bash
git clone https://github.com/Marcdur/tripleten-sprint-07-chicago-taxi.git
cd tripleten-sprint-07-chicago-taxi
```

Instale as bibliotecas necessárias:

```bash
pip install pandas numpy matplotlib seaborn scipy jupyter
```

Disponibilize os três arquivos CSV no diretório `/datasets/` e abra o notebook:

```bash
jupyter notebook projeto-7-chicago-taxi.ipynb
```

## Arquivo principal

- [`projeto-7-chicago-taxi.ipynb`](./projeto-7-chicago-taxi.ipynb): notebook com carregamento dos dados, análise exploratória, visualizações, teste estatístico e conclusões.

## Observação

Este é um estudo educacional baseado em uma amostra de viagens e em resultados de consultas SQL. As conclusões refletem o período e as variáveis disponíveis nos arquivos do projeto; portanto, não devem ser interpretadas como uma descrição definitiva de toda a operação de táxis de Chicago.

---

## English version

Project developed during **Sprint 7 of the TripleTen Data Science Bootcamp**, using Python, pandas, Matplotlib, Seaborn and SciPy.

## About the project

This project analyzes taxi trips in Chicago with a focus on exploratory data analysis and testing an operational hypothesis. The study uses results from SQL queries and investigates which companies concentrate the most rides, which neighborhoods appear most frequently as destinations, and whether weather conditions influence trip duration between the Loop and O'Hare International Airport.

The objective is to transform the data into useful information to understand transportation demand and to assess whether trips made on rainy Saturdays behave differently from trips made on Saturdays under other conditions.

## Objectives

The project was developed to:

- import and inspect the results of the SQL queries;
- check dimensions, data types, missing values and descriptive statistics;
- identify the top ten taxi companies by number of rides;
- identify the top ten Chicago neighborhoods by average number of completed trips;
- build charts of companies and neighborhoods to facilitate result interpretation;
- separate Loop-to-O'Hare trips according to weather conditions;
- test the hypothesis about the average duration of trips on rainy Saturdays;
- explain the null and alternative hypotheses, the significance level and the decision criterion.

## Data used

The notebook uses three result files provided by the project:

| Arquivo | Conteúdo |
|---|---|
| `project_sql_result_01.csv` | Número de corridas por empresa de táxi nos dias 15 e 16 de novembro de 2017 |
| `project_sql_result_04.csv` | Bairros de Chicago e número médio de viagens que terminaram em cada bairro em novembro de 2017 |
| `project_sql_result_07.csv` | Data e hora de início, condições meteorológicas e duração das viagens do Loop para O'Hare |

**The datasets are not included in this repository.** They must be made available separately in the `/datasets/` directory, according to the original course instructions.

## Steps performed

### 1. Exploratory analysis

The first two files are loaded and evaluated for format, data types, missing values and descriptive statistics. The notebook then sorts companies by number of rides and neighborhoods by average number of destinations.

### 2. Visualizations

Bar charts are created to show the taxi companies with the highest ride volume and the ten neighborhoods with the highest average number of completed trips. The visualizations allow identification of demand concentration and regions with higher drop-off flow.

### 3. Hypothesis test

The third file is used to compare the duration of Loop-to-O'Hare trips on rainy Saturdays and on Saturdays with other weather conditions. The statistical test is performed with independent samples, the significance level is set in the notebook and the interpretation is based on the p-value.

The formulation adopted is:

- **Null hypothesis (H₀):** the mean duration of trips on rainy Saturdays is equal to the mean duration of trips on non-rainy Saturdays;
- **Alternative hypothesis (H₁):** the mean duration of trips on rainy Saturdays is different from the mean duration of trips on non-rainy Saturdays.

The decision criterion is to reject H₀ when the p-value is less than the chosen significance level. The justification for the test and the conclusion are recorded in the notebook.

## Main findings

The analysis shows a strong concentration of rides in a small group of companies, with emphasis on Flash Cab. Among destinations, the Loop leads by a wide margin, followed by River North, Streeterville and West Loop, which confirms the importance of downtown Chicago as an arrival area.

The statistical test evaluates whether rain changes the duration of trips between the Loop and O'Hare. The notebook's conclusion is based on the observed p-value and should be interpreted specifically for the set of Saturdays analyzed, without automatic generalization to all days or routes.

## Result

The outcome is a diagnosis of taxi demand in Chicago with a ranking of companies, a ranking of the ten main destination neighborhoods and a test of the hypothesis about the duration of Loop-to-O'Hare trips on rainy Saturdays. The visualizations highlight the concentration of flow in the Loop and other central neighborhoods, while the statistical conclusion should be read according to the p-value and the significance level recorded in the notebook.

## What I learned

The project consolidated the connection between SQL query results and analysis in Python, including slicing, grouping, sorting, chart building and formulation of null and alternative hypotheses. It also reinforced correct interpretation of p-value, alpha and limitations of generalization.

## Possible improvements

As an evolution, it would be possible to document the original SQL queries, present confidence intervals and effect sizes, compare weekdays and peak hours as well, and use robust or non-parametric tests as a sensitivity analysis. Including quantitative precipitation and travel time would allow a more detailed operational investigation.

## Technologies used

- Python 3
- pandas
- NumPy
- Matplotlib
- Seaborn
- SciPy
- Jupyter Notebook
- SQL and GitHub

## How to run

Clone the repository:

```bash
git clone https://github.com/Marcdur/tripleten-sprint-07-chicago-taxi.git
cd tripleten-sprint-07-chicago-taxi
```

Install the required libraries:

```bash
pip install pandas numpy matplotlib seaborn scipy jupyter
```

Make the three CSV files available in the `/datasets/` directory and open the notebook:

```bash
jupyter notebook projeto-7-chicago-taxi.ipynb
```

## Main file

- [`projeto-7-chicago-taxi.ipynb`](./projeto-7-chicago-taxi.ipynb): notebook with data loading, exploratory analysis, visualizations, statistical test and conclusions.

## Note

This is an educational study based on a sample of trips and on results from SQL queries. The conclusions reflect the period and variables available in the project files; therefore, they should not be interpreted as a definitive description of the entire Chicago taxi operation.

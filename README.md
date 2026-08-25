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

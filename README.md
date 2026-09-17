# NYC_Data_Taxi_Analytics
# 🚕 NYC Taxi Analytics

### Análise de demanda, comportamento das corridas e otimização operacional do serviço de táxis de Nova York

> Um projeto de Data Analytics + Operations Research desenvolvido a partir de dados reais de corridas de táxi de Nova York.


##  Sobre o projeto

Como a demanda por táxis varia ao longo do dia?

Quais períodos concentram o maior número de corridas?

Como fatores como distância, duração e horário se relacionam com o valor das viagens?

E, a partir desses padrões, como a operação poderia distribuir seus recursos de forma mais eficiente?

Este projeto busca responder essas perguntas utilizando dados reais do **NYC Taxi & Limousine Commission (TLC)**, combinando **Python, Pandas, SQL, Power BI e técnicas de otimização**.

O objetivo não é apenas visualizar os dados, mas transformar milhões de registros de corridas em informações capazes de apoiar decisões operacionais.


##  Objetivos

- Analisar o comportamento da demanda por táxis;
- Identificar padrões temporais de utilização;
- Avaliar a relação entre distância, duração e valor das corridas;
- Identificar períodos de maior e menor demanda;
- Detectar e tratar inconsistências presentes nos dados;
- Construir indicadores e dashboards interativos;
- Explorar uma abordagem de otimização para distribuição de recursos;
- Transformar dados brutos em informações para suporte à decisão.



##  Dados

O projeto utiliza os registros de **Yellow Taxi Trip Records — janeiro de 2016**, disponibilizados pela NYC TLC.

O dataset contém mais de **10 milhões de registros** e informações como:

- data e hora de embarque e desembarque;
- quantidade de passageiros;
- distância da viagem;
- localização de origem e destino;
- tipo de tarifa;
- forma de pagamento;
- valor da tarifa;
- gorjeta;
- pedágios;
- valor total da corrida.

Devido ao tamanho do dataset, o arquivo CSV não é armazenado diretamente neste repositório.

 **Fonte dos dados:**  
NYC Taxi & Limousine Commission (TLC)



## Tratamento dos dados

Antes da análise, foi realizada uma etapa de preparação dos dados para identificar registros inconsistentes e valores potencialmente inválidos.

Foram analisados casos como:

- durações negativas ou iguais a zero;
- distâncias iguais a zero;
- valores totais negativos;
- corridas com desembarque fora do período analisado;
- distâncias extremamente elevadas;
- tarifas incompatíveis com os demais registros;
- registros duplicados.

Após o processo de limpeza:

| Etapa | Registros |
|---|---:|
| Dataset original | 10.906.858 |
| Registros removidos | 70.260 |
| Dataset analisado | **10.836.598** |
| Dados preservados | **99,36%** |

O tratamento foi realizado buscando preservar a maior quantidade possível de informações sem comprometer a qualidade das análises.



##  Análise exploratória

A análise exploratória investiga diferentes dimensões do comportamento das corridas.

###  Demanda ao longo do dia

A quantidade de corridas apresenta forte variação durante o dia, com crescimento ao longo da manhã e concentração da demanda no período da tarde.

O maior volume observado ocorre próximo ao final do horário comercial, enquanto a madrugada apresenta os menores volumes.

###  Demanda por dia da semana

A demanda também apresenta diferenças entre os dias da semana.

A sexta-feira concentra um dos maiores volumes de corridas, enquanto a segunda-feira apresenta um dos menores.

###  Dia × hora

A combinação entre dia da semana e horário permite identificar períodos específicos de concentração de demanda.

Essa análise é especialmente relevante para decisões relacionadas à alocação de veículos e planejamento operacional.



##  Identificação de anomalias

Além de buscar padrões, o projeto também investiga comportamentos inesperados nos dados.

Foram encontrados registros com:

- distâncias incompatíveis com a duração da viagem;
- tarifas extremamente elevadas;
- viagens com duração de vários dias;
- valores negativos;
- distâncias superiores a centenas ou milhares de quilômetros.

Esses casos demonstram a importância da etapa de **Data Cleaning** antes da construção de indicadores e modelos analíticos.



##  Dashboard

Os resultados da análise serão apresentados em um dashboard desenvolvido no **Power BI**, organizado em diferentes perspectivas:

### Overview
- Total de corridas
- Receita total
- Distância percorrida
- Valor médio das corridas
- Duração média
- Evolução temporal

### Demand
- Corridas por hora
- Corridas por dia da semana
- Heatmap de demanda
- Distribuição temporal das viagens

### Revenue & Trips
- Receita por período
- Relação entre distância e valor
- Relação entre duração e valor
- Distribuição dos valores das corridas

### Optimization
- Demanda observada
- Distribuição de recursos
- Utilização da frota
- Demanda atendida e não atendida



## ⚙️ Otimização operacional

A etapa de otimização busca utilizar os padrões identificados na análise para formular um problema de decisão.

A ideia é considerar uma quantidade limitada de veículos e determinar como distribuí-los entre diferentes regiões ou períodos de demanda.

O modelo pode considerar objetivos como:

- reduzir demanda não atendida;
- diminuir desequilíbrios entre regiões;
- melhorar a utilização da frota;
- reduzir deslocamentos desnecessários.

Dessa forma, a análise deixa de responder apenas:

> **"O que aconteceu?"**

e passa também a investigar:

> **"Como os recursos poderiam ser distribuídos?"**



## 🛠️ Tecnologias

| Tecnologia | Aplicação |
|---|---|
| 🐍 Python | Tratamento e análise dos dados |
| 🐼 Pandas | Manipulação do dataset |
| 📊 Matplotlib | Visualização exploratória |
| 🗄️ SQL | Consultas e análise estruturada |
| 📈 Power BI | Dashboard e visualização interativa |
| ⚙️ Operations Research | Formulação do problema de otimização |
| 🔧 Git/GitHub | Versionamento e documentação |


└── .gitignore

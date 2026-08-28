🏆 Desafio FIFA World Cup — Data Engineering & Analytics

Projeto de Engenharia de Dados desenvolvido para transformar dados históricos e dados da Copa do Mundo FIFA 2026 em uma solução analítica estruturada, utilizando Python, PySpark, SQL, Google Colab, Google Drive e Power BI.

O desafio foi construído seguindo a Arquitetura Medalhão (Medallion Architecture), organizando o processamento dos dados em camadas Bronze, Silver e Gold, desde a ingestão e tratamento dos dados brutos até a criação de um modelo dimensional preparado para análises e dashboards.

🎯 Objetivo

Construir um pipeline completo de dados capaz de:

Ingerir dados históricos da Copa do Mundo;
Processar e padronizar os dados utilizando PySpark;
Aplicar regras de qualidade e transformação;
Consolidar partidas, seleções, artilheiros e fixtures da Copa do Mundo 2026;
Criar tabelas dimensionais e fatos na camada Gold;
Disponibilizar os dados para análise no Power BI;
Demonstrar na prática conceitos de Data Engineering, Data Modeling e Business Intelligence.
🏗️ Arquitetura do Projeto
                  ┌─────────────────────┐
                  │   Dados de Origem   │
                  │ CSV / Google Drive  │
                  └──────────┬──────────┘
                             │
                             ▼
                    ┌────────────────┐
                    │     BRONZE     │
                    │ Dados Brutos   │
                    └───────┬────────┘
                            │
                            ▼
                    ┌────────────────┐
                    │     SILVER     │
                    │ Tratamento     │
                    │ Padronização   │
                    │ Validação      │
                    └───────┬────────┘
                            │
                            ▼
                    ┌────────────────┐
                    │      GOLD      │
                    │ Modelo Dim.    │
                    │ Fatos + Dim.   │
                    └───────┬────────┘
                            │
                            ▼
                    ┌────────────────┐
                    │    POWER BI    │
                    │ Dashboard      │
                    │ KPIs & Análises│
                    └────────────────┘
🥉 Camada Bronze

Responsável pela ingestão dos dados em seu formato original, preservando os dados de origem para posterior processamento.

🥈 Camada Silver

Nesta camada são realizados:

Tratamento de valores nulos;
Padronização de nomes;
Conversão de tipos;
Tratamento de datas;
Validação dos dados;
Criação de indicadores derivados;
Padronização das informações das partidas;
Consolidação dos dados históricos e dos fixtures de 2026.

Principais tabelas:

silver_matches
silver_editions
silver_teams_2026
silver_top_scorers
silver_fixtures_2026
🥇 Camada Gold

A camada Gold transforma os dados tratados em estruturas analíticas utilizando conceitos de modelo dimensional e Star Schema.

Principais dimensões:

dim_time
dim_data
dim_estadio
dim_localidade

E tabelas fato:

fato_partida

A dim_time, por exemplo, reúne informações como:

Seleção;
Grupo;
Confederação;
Ranking FIFA;
Técnico;
Melhor resultado em Copas;
Participação na Copa de 2026.
🛠️ Tecnologias utilizadas
Python
PySpark
Apache Spark
SQL
Pandas
Google Colab
Google Drive
Power BI
Git & GitHub
📊 Análises e Indicadores

O modelo permite desenvolver análises como:

Total de partidas;
Total de gols;
Média de gols por partida;
Vitórias, derrotas e empates;
Desempenho das seleções;
Ranking de seleções;
Artilheiros;
Desempenho por edição;
Análise por fase da competição;
Análise por estádio e localização;
Comparação histórica entre Copas do Mundo;
Acompanhamento dos fixtures da Copa do Mundo 2026.
🚀 Conceitos de Data Engineering aplicados

Este projeto demonstra na prática conhecimentos em:

Arquitetura Medalhão;
ETL / ELT;
Data Cleaning;
Data Quality;
Transformação distribuída com PySpark;
Modelagem dimensional;
Star Schema;
Surrogate Keys;
DataFrames;
Window Functions;
Joins;
Unions;
Tratamento de dados históricos;
Preparação de dados para BI.
📁 Estrutura do Repositório

🎯 Resultado

O projeto demonstra a construção de uma solução completa de dados, partindo de arquivos brutos até um modelo analítico estruturado e preparado para visualização no Power BI.

Além de servir como projeto de portfólio, o desafio busca reproduzir uma situação próxima ao ambiente profissional de Engenharia de Dados, envolvendo ingestão, transformação, qualidade, modelagem e disponibilização dos dados para consumo analítico.

👨‍💻 Autor

Luvuvamo Carlos
Data Engineer | Python | PySpark | SQL | Azure | Databricks | Google Colab | AWS | Power BI

#DataEngineering #PySpark #Python #SQL #ApacheSpark #DataLake #MedallionArchitecture #DataModeling #PowerBI #FIFAWorldCup #GitHub #DataAnalytics

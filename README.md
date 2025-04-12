
# Análise e Modelagem de Dados sobre Obesidade

Este repositório contém a estruturação, modelagem e análise de um conjunto de dados voltado à obesidade, com o objetivo de investigar os fatores comportamentais, físicos e familiares que influenciam o diagnóstico da condição. O trabalho foi realizado em ambiente Databricks utilizando PySpark e SQL.

## Objetivo

Construir um modelo de dados relacional em formato Snowflake, realizar o pipeline de ETL (Extração, Transformação e Carga) e aplicar análises estatísticas univariadas e bivariadas com o intuito de:

- Entender como a obesidade se distribui entre diferentes perfis.
- Avaliar fatores associados ao diagnóstico, como faixa etária, histórico familiar, hábitos alimentares e estilo de vida.
- Apoiar o desenvolvimento de políticas públicas e futuros modelos preditivos.

## Dataset utilizado

- Nome: ObesityDataSet_raw_and_data_sinthetic.csv  
- Fonte: [Kaggle - Obesity Dataset](https://www.kaggle.com/datasets/abdelrahman16/obesity-dataset)  
- Autores: Palechor, F. M., & Manotas, I. M. (2019)  
- Observação: 77% dos dados foram gerados sinteticamente usando SMOTE; 23% foram coletados via web.

## Estrutura do Projeto

O notebook segue as seguintes etapas:

1. Modelagem de Dados
   - Modelo conceitual e lógico (Snowflake)
   - Normalização até BCNF
   - Criação do modelo físico via SQL

2. Pipeline ETL com PySpark
   - Extração e padronização dos dados
   - Criação das dimensões e da tabela fato
   - Escrita segura no Data Warehouse com Delta Lake

3. Verificação da Qualidade e Validação Estrutural
   - Presença de valores nulos ou zeros inconsistentes
   - Integridade referencial entre fato e dimensões

4. Análises
   - Análise univariada (distribuição de variáveis)
   - Análise bivariada (cruzamento entre atributos e diagnóstico)
   - Interpretação com apoio de literatura científica e fontes oficiais (CDC, PAHO)

## Resultados Destacados

- O histórico familiar de sobrepeso foi o fator com maior associação aos níveis mais graves de obesidade.
- Alguns atributos comportamentais apresentaram valores inconsistentes, indicando possíveis efeitos da geração sintética dos dados.
- O modelo Snowflake desenvolvido permite consultas SQL otimizadas e estrutura base para projetos de machine learning supervisionado.

## Trabalhos Futuros

- Aplicar o modelo a dados 100% reais para reduzir viés.
- Enriquecer o conjunto com variáveis de qualidade nutricional.
- Integrar visualizações com Power BI ou Tableau.
- Ampliar o uso do modelo para análise preditiva em novos cenários.

## Projeto complementar

Um modelo preditivo com machine learning também foi criado anteriormente com base neste dataset, disponível em:

[Projeto de Machine Learning - Predição de Obesidade (Colab)](https://github.com/TPRibeiro/mvp_mla/blob/main/Final.ipynb)

## Tecnologias Utilizadas

- Databricks (Community Edition)
- PySpark
- Delta Lake
- SQL (SparkSQL)
- Pandas (para construção do dicionário de dados)
- Markdown

## Observações

- O dataset apresenta viés devido à geração sintética via SMOTE. As conclusões devem ser interpretadas com cautela.
- O notebook foi exportado com as células executadas para preservar os outputs e facilitar a visualização.
- Alguns arquivos como imagens e dicionários não foram incorporados automaticamente durante a exportação do notebook. Por isso, os seguintes arquivos foram adicionados manualmente ao repositório:
  - `figura1.png` – Diagrama do modelo conceitual
  - `figura2.png` – Diagrama do modelo lógico
  - `dicionario.csv` – Dicionário de dados original
  - `dicionario2.csv` – Dicionário com estatísticas (mínimos, máximos, médias)

Esses arquivos podem ser referenciados diretamente nos notebooks conforme necessário.

## Contato

Caso tenha dúvidas ou sugestões, fique à vontade para abrir uma issue ou entrar em contato.

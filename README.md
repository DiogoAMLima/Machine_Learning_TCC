# Criação de modelos de Machine Learning para previsão e prevenção de doenças

Etapa de desenvolvimento de codigo para tratamento dos dados e técnicas de `Machine Learning` para diagnóstico da doença câncer e tambem toda a implementação da arquitetura medallion para armazenamento dos datasets na cloud `Azure`

## Linguagens e ferramentas utilizadas para a criação desse projeto
- Azure
- Databricks
- Azure Data Lake Storage Gen2
- Python
- Spark
- PySpark
- Pandas
- Bibliotecas de aprendizado de maquina

## Arquitetura do Projeto
O projeto utiliza a arquitetura medallion trazendo as camadas `bronze`, `silver` e `gold` para armazenamento 

![Arquitetura_Medalhão drawio](https://github.com/thiagothr/Machine_Learning_TCC/assets/72639507/6c33f16f-3bd8-4988-a355-6b56c1e31da1)


antes de tudo foi criado recursos no ambiente da `Azure` para conseguirmos presseguir com todo o armazenamento na nuvem. Depois de todos os recuros criados, criamos o armazenamento no storage account utilizando o `Data Lake Storage Gen 2`
e fizemos a criação das camadas `bronze`, `silver` e `gold`.

![Captura de tela 2024-05-19 204724](https://github.com/thiagothr/Machine_Learning_TCC/assets/72639507/98e13085-85fc-43bb-8902-6bec23d8eefb)

Após a criação das camadas fizemos o upload dos datasets `Cancer_Data.csv` e `Dados_dummies.csv` para a cada `Bronze` conhecida como camada `Raw` onde todo os dados brutos vão ser armazenados nessa camada para ser enviada ao `Databricks`

## Databricks
como falado anteriormente após todo o armazenamento dos dados no datalake do azure criamos o workspace para acessar o `databricks` para realizar toda a etapa de tratamento dos dados é criação dos modelos de `Machine learning`.
abaixo podemos ver criação e configuração do cluster onde vamos realizar todo nosso projeto.
![databricks](https://github.com/thiagothr/Machine_Learning_TCC/assets/72639507/8c7f6f87-9d7b-4e38-a6e9-7c43ec06fa9b)
depois do cluster criado agora vamos para as etapas importantes que é o tratamento dos dados e a criação dos modelos de `ML.

### Etapa desenvolvimento
antes de realizar qualquer tratamento é importante levar os dados do nosso datalake para o databricks e para isso precisamos montar uma conexão entre o databricks e o datalake para pordemos extrair e tratar os dados da nossa camada `bronze`![mount_databricks](https://github.com/thiagothr/Machine_Learning_TCC/assets/72639507/87e961c9-34c5-4f76-9ed1-c91e42b42b4c)
feito a criação dessa conexão agora podemos tratar os dados e criar os modelos todo o script criado para o dataset `Cancer_Data.csv` e `Dados_dummies.csv` se encontra `Machine_Learning_Cancer.ipynb` e `Machine_Learning_Cancer2.ipynb`.

## Processos de Machine Learning
abaixo mostraremos um processo de machine learning onde realizamos cada etapa do ciclo apresentado abaixo.

![ciclo ml](https://github.com/thiagothr/Machine_Learning_TCC/assets/72639507/420bf780-67be-4297-835c-defda3a941c6)


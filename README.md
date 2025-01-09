# Documentação do Projeto

## Table of Contents

1. [Introdução](#introduction)
2. [Estrutura](#app-structure)
3. [Explicação dos Ficheiros](#files-explanation)
    1. [DataUnderstanding.ipynb](#dataunderstandingipynb)
    2. [DataPreparation.ipynb](#datapreparationipynb)
    3. [Modeling.ipynb](#modelingipynb)
    4. [Evaluation.ipynb](#evaluationipynb)
    5. [Deployment.ipynb](#deploymentipynb)


4. [Como correr ?](#HowtoRuntheApp)

## Introdução
Este projeto tem como objetivo desenvolver um modelo de previsão de risco de doenças cardiovasculares baseado na metodologia CRISP-DM (Cross-Industry Standard Process for Data Mining) para garantir uma abordagem estruturada e sistemática. Serão aplicados algoritmos de aprendizagem supervisionada e não supervisionada para análise e desenvolvimento do modelo. 

## Estrutura

```
  ProjetoIAA_Folder      
├── data
│   ├── CVC_10reduced_strategy1.csv
│   └── CVC_10reduced_strategy2.csv
├── notebooks
│   │   ├── DataUnderstanding.ipynb
│   │   ├── DataPreparation.ipynb
│   │   └── Modeling.ipynb
├── .vscode
│   │   └── setting.json
├── .gitignore
├── .gitattributes
├── README.md
├── requirements.txt
```

## Explicação dos Ficheiros
### [DataUnderstanding.ipynb](notebooks/DataUnderstanding.ipynb)
Este Jupyter Notebook tem como objetivo fornecer uma compreensão inicial e análise de um conjunto de dados relacionados a doenças cardiovasculares (DCV). O dataset contém várias métricas de saúde e informações demográficas.

Esta seção fornece uma visualização e análise preliminar do conjunto de dados. Inclui:
* Um resumo da estrutura do dataset, incluindo o número de linhas e colunas;
* Estatísticas descritivas como média, desvio padrão, mínimo e máximo para colunas numéricas;
* Uma visão geral dos primeiros registros para entender o conteúdo.

#### Importações
O notebook começa importa bibliotecas essenciais para manipulação e visualização de dados:

        import pandas as pd
        import numpy as np
        import matplotlib.pyplot as plt
        import seaborn as sns

#### Carregamento do *dataset*

        data_path = '../data/'
        cvd_df = pd.read_csv(data_path + 'CVD_cleaned.csv')


### [DataPreparation.ipynb](notebooks/DataPreparation.ipynb)

### [Modeling.ipynb](notebooks/Modeling.ipynb)
### [Evaluation.ipynb](notebooks/Evaluation.ipynb)
### [Deployment.ipynb](notebooks/Deployment.ipynb)



## Como correr ?

Para correr o código, siga os seguintes passos:
#### 1. Fazer clone do repositório remoto
        Command: git clone https://github.com/tjpoa/ProjetoIAA.git

#### 2. Criar ambiente virtual
         python -m venv venv

#### 3. Ativar ambiente virtual
         python\Scripts\activate

#### 4. Instalar dependências
         pip install -r requirements.txt



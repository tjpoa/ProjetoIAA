# Documentação do Projeto

## Índice

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
│   ├── CVD_cleaned.csv
│   └── CVD_normalized_discretized_processed.csv
├── notebooks
│   ├── DataUnderstanding.ipynb
│   ├── DataPreparation.ipynb
│   ├── Deployment.ipynb
│   ├── Evaluation.ipynb
│   └── Modeling.ipynb
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
O notebook importa bibliotecas essenciais para manipulação e visualização de dados:

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
Este Jupyter Notebook implementa um modelo de *Decision Tree* para a predição de doenças cardiovasculares e realiza uma análise dos *clusters* gerados pelo K-Means. O objetivo principal é criar um modelo preditivo para identificar a probabilidade de ocorrência de doenças cardiovasculares com base no *dataset*. Além disso, são aplicados métodos de visualização para entender melhor a distribuição dos dados e os resultados dos clusters.

#### Importações
O notebook importa bibliotecas essenciais para manipulação e visualização de dados:

        import pandas as pd
        import numpy as np
        import seaborn as sns
        import matplotlib.pyplot as plt
        from sklearn.tree import DecisionTreeClassifier
        from sklearn.metrics import accuracy_score, classification_report, confusion_matrix
        from sklearn.preprocessing import StandardScaler
        from sklearn.decomposition import PCA
        from sklearn.cluster import KMeans

#### Carregamento do *dataset* normalizado

        data_path = '../data/' 
        cvd_df_processed = pd.read_csv(data_path + 'CVD_normalized_discretized_processed.csv')

#### Pré-processamento dos Dados
* O código divide as variáveis em atributos (X) e o alvo (y), sendo que o alvo é a variável `Heart_Disease`, que indica se o paciente tem ou não CVD.

#### *Decision Tree* 
* É utilizado um modelo de *Decision Tree* com profundidade máxima de 5 (max_depth=5).

* O modelo é treinado nos dados e, em seguida, avaliado com a precisão (`accuracy_score`) e um relatório de classificação (`classification_report`), além de gerar uma matriz de confusão para visualizar a performance do modelo.

#### *K-Means*

*  Para reduzir o tamanho do conjunto de dados e melhorar a performance, é realizada uma amostragem de 80% dos dados.

* O algoritmo *K-Means* é usado para dividir os dados em 3 clusters, e os resultados são visualizados através de gráficos de dispersão, com a variável alvo `Heart_Disease` e outras variáveis de interesse.










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



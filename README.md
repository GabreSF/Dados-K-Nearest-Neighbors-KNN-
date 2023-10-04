# Resumo do Projeto de Análise de Dados com K-Nearest Neighbors (KNN)

## Objetivo do Projeto
Este projeto envolve a análise de um conjunto de dados usando a técnica de K-Nearest Neighbors (KNN) para classificação. O objetivo principal é construir um modelo de machine learning capaz de prever a classe de amostras de um conjunto de dados, tendo como base as características presentes nesses dados.

## Passos Realizados até o Momento

### 1. Carregamento do Conjunto de Dados
   - Foi carregado um conjunto de dados chamado "creditcard_2023.csv" usando a biblioteca Pandas. O conjunto de dados provavelmente contém informações sobre transações de cartão de crédito.

### 2. Exploração Inicial dos Dados
   - Foram examinadas as dimensões do conjunto de dados com `df.shape`.
   - Foi visualizado o início do conjunto de dados com `df.head(10)` para entender suas colunas e formatos.
   - Foi verificada a presença de valores nulos com `df.isnull().sum()`.
   - Foram identificadas duplicatas com `df[df.duplicated()]`.

### 3. Pré-processamento dos Dados
   - As características foram isoladas em `x` e a variável de destino em `y`.
   - As características foram normalizadas usando o Min-Max Scaling.
   - Foi realizada a redução da dimensionalidade das características usando a Análise de Componentes Principais (PCA).

### 4. Divisão dos Dados em Treinamento e Teste
   - Os dados foram divididos em conjuntos de treinamento (`x_train` e `y_train`) e teste (`x_test` e `y_test`) com 90% para treinamento e 10% para teste.

### 5. Avaliação de Modelos KNN com Diferentes Valores de `k`
   - Foram treinados modelos KNN para diferentes valores de `k` (número de vizinhos) com distância ponderada e métrica de distância Euclidiana.
   - A precisão dos modelos foi calculada em relação ao conjunto de teste para cada valor de `k`.

### 6. Treinamento do Modelo KNN Final
   - Um modelo KNN com `k=3`, distância ponderada e métrica de distância Euclidiana foi treinado com o conjunto de treinamento final.

### 7. Avaliação do Modelo Final
   - O modelo KNN final foi avaliado com base no conjunto de teste, e a precisão foi calculada como uma métrica de desempenho.

## Resultado até o Momento
O modelo KNN final alcançou uma precisão de aproximadamente 99.19% no conjunto de teste, o que sugere um desempenho muito bom na tarefa de classificação. No entanto, ainda é importante realizar análises adicionais para avaliar outras métricas de desempenho e considerar a adequação do modelo às necessidades específicas do projeto.

## Passos Futuros
- Avaliação mais detalhada do desempenho do modelo, incluindo métricas como matriz de confusão, F1-score e recall.
- Verificação da possibilidade de overfitting e ajuste de hiperparâmetros do modelo.
- Implementação de validação cruzada para garantir a robustez do modelo.
- Consideração de qualquer análise adicional necessária para atender aos objetivos específicos do projeto.

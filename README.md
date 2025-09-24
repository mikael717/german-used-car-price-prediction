# 🚗 Análise e Predição de Preços de Carros Usados na Alemanha

Este projeto realiza uma análise exploratória de dados e constrói modelos de Machine Learning para prever o preço de carros usados na Alemanha, focando em um subconjunto específico de veículos para modelagem.

## Objetivo 🔗

O principal objetivo deste projeto é:

1.  Realizar uma análise descritiva dos dados para entender as características do mercado de carros usados na Alemanha.
2.  Identificar as features mais importantes que influenciam o preço dos carros.
3.  Desenvolver e avaliar modelos de regressão para prever o preço de venda de carros usados.

## Dados 📊

Os dados utilizados neste projeto são provenientes do arquivo `germany-used-cars-2023.csv`, obtido no Kaggle:


O conjunto de dados contém informações sobre diversos carros usados, incluindo:

*   Marca (`brand`)
*   Modelo (`model`)
*   Cor (`color`)
*   Data de registro (`registration_date`)
*   Ano (`year`)
*   Preço em euros (`price_in_euro`)
*   Potência em kW (`power_kw`)
*   Potência em PS (`power_ps`)
*   Tipo de transmissão (`transmission_type`)
*   Tipo de combustível (`fuel_type`)
*   Consumo de combustível (`fuel_consumption_l_100km`, `fuel_consumption_g_km`)
*   Quilometragem em km (`mileage_in_km`)
*   Descrição da oferta (`offer_description`)

Durante o pré-processamento, foram criadas novas features como a idade do carro (`car_age`) e algumas colunas foram removidas para simplificar a análise e modelagem.

## Análise Exploratória de Dados (EDA) 🔍

A análise exploratória incluiu:

*   Estatísticas descritivas das variáveis numéricas (`price_in_euro`, `mileage_in_km`, `car_age`).
*   Visualização da distribuição das variáveis numéricas através de histogramas.
*   Identificação de outliers usando boxplots.
*   Análise da correlação entre as variáveis numéricas através de uma matriz de correlação e heatmap, mostrando a relação entre preço, quilometragem e idade do carro.

## Pré-processamento e Seleção de Dados 🛠️

Para o desenvolvimento dos modelos de Machine Learning, o conjunto de dados foi filtrado para incluir apenas carros com características específicas (neste caso, Volkswagen Golf com 150 PS, transmissão manual, combustível a gasolina e com menos de 11 anos de idade). Variáveis categóricas foram convertidas usando One-Hot Encoding.

## Modelagem de Machine Learning 🤖

Foram treinados e avaliados modelos de regressão para prever o preço dos carros:

*   **Linear Regression:** Um modelo base para comparação.
*   **Random Forest Regressor:** Um modelo de ensemble que geralmente apresenta bom desempenho em tarefas de regressão.
*   **Gradient Boosting Regressor:** Outro modelo de ensemble poderoso.

Os modelos foram avaliados usando métricas como R² e MAPE (Mean Absolute Percentage Error).

## Análise de Importância das Features 🔥

Utilizando o modelo RandomForestRegressor, foi analisada a importância das diferentes features para a predição do preço, indicando quais variáveis tiveram maior influência no resultado do modelo.

## Como Executar o Notebook ▶️

1.  Certifique-se de ter as bibliotecas Python necessárias instaladas (pandas, numpy, seaborn, matplotlib, sklearn). Você pode instalá-las usando pip.

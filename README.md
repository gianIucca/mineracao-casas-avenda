# Predição de Preços de Imóveis (Web Scraping + Machine Learning) para análise do mercado imobiliário - Amsterdam <br>
## Visão Geral do Projeto <br>

Sistema completo de análise do mercado imobiliário de Amsterdam, combinando web scraping do site Pararius.com com machine learning para predição de preços de aluguel. O projeto alcançou um R² de 0.964 utilizando CatBoost Regressor após otimização de hiperparâmetros. <br>

# Arquitetura do Projeto <br> 
## Coleta de Dados (Web Scraping) <br>

Site alvo: Pararius.com (portal imobiliário de Amsterdam) <br>
Dados coletados: 509 apartamentos únicos <br>
Ferramentas: BeautifulSoup, requests <br>
Features extraídas: Título, localização, preço, tamanho, número de quartos, mobília <br>

## Processamento e Limpeza de Dados <br>

Classe Formatador: Pipeline automatizado de limpeza <br>
Transformações: Remoção de duplicatas, normalização de texto, conversão de tipos <br>
Feature Engineering: Separação de informações compostas em colunas específicas <br>
Encoding: One-hot encoding para variáveis categóricas (72 localizações, tipos de mobília) <br>

## Tecnologias Utilizadas <br>

Web Scraping: BeautifulSoup, requests <br>
Processamento de Dados: pandas, numpy <br>
Machine Learning: scikit-learn, xgboost, lightgbm, catboost <br>
Visualização: seaborn, matplotlib <br>

## Pipeline de Processamento de Dados <br>

Modelos Avaliados: 12 algoritmos de regressão testados: <br>

RandomForestRegressor, LinearRegression, Ridge, Lasso <br>
XGBRegressor, CatBoostRegressor, LGBMRegressor <br>
DecisionTreeRegressor, MLPRegressor, KNeighborsRegressor <br>
SVR, GaussianProcessRegressor <br>

Resultados e Performance <br>
Métricas do Modelo Final (CatBoost) <br>

R² Score: 0.964 <br>
MAE: 448.95 EUR <br>
RMSE: 986.83 EUR <br>
MSE: 973,831.88 <br>

 
## Análise Exploratória de Dados <br>

Localizações mais caras: Zuidas (€4,828), Willemspark (€4,586) <br>
Localizações mais acessíveis: Waterlandpleinbuurt (€1,295), Holendrecht (€1,400) <br>
Distribuição por mobília: Análise de preços por tipo de mobiliário <br>

## Web Scraping e Engenharia de Dados <br>

Extração automatizada de dados de sites imobiliários <br>
Tratamento de paginação e dados duplicados <br>
Pipeline robusto de limpeza e transformação de dados <br>
Validação e normalização de dados coletados <br>

## Machine Learning e Ciência de Dados <br>

Comparação sistemática de 12 algoritmos de regressão <br>
Feature engineering com variáveis categóricas de alta cardinalidade <br>
Otimização de hiperparâmetros com validação cruzada <br>
Avaliação rigorosa com múltiplas métricas <br>

## Engenharia de Software <br>

Arquitetura orientada a objetos (classe Formatador) <br>
Código modular e reutilizável <br>
Tratamento de exceções e validação de dados <br>
Pipeline automatizado end-to-end <br>

## Estrutura dos Dados <br>
Features Finais (81 colunas) <br>

Numéricas: Preço (EUR), tamanho (m²), quartos, código postal <br>
Categóricas: 72 localizações de Amsterdam, tipos de mobília <br>
Target: Preço de aluguel mensal em euros <br>

Tecnologias: Python, BeautifulSoup, Pandas, Scikit-learn, CatBoost, XGBoost <br> 
Competências: Web Scraping, Machine Learning, Data Engineering, Análise de Mercado, Feature Engineering

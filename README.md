# 🏠 House Prices: Advanced Regression Techniques

[![en](https://img.shields.io/badge/lang-en-red.svg)](https://github.com/smartielo/house-prices-analysis#english-description)
[![pt-br](https://img.shields.io/badge/lang-pt--br-green.svg)](https://github.com/smartielo/house-prices-analysis#descri%C3%A7%C3%A3o-em-portugu%C3%AAs)

<a name="english-description"></a>
## 🇺🇸 English Description

### Project Overview
This project is a complete data science solution for the Kaggle competition: **"House Prices - Advanced Regression Techniques"**.
The goal is to predict the final price of each home in Ames, Iowa, using 79 explanatory variables. We successfully built a model with **~89% accuracy (R² Score)** on the validation set.

### 🛠️ Techniques & Workflow
1.  **Data Cleaning & Imputation:**
    * Identified that `NaN` in columns like `PoolQC`, `Fence`, and `Alley` meant "Absence of feature", not missing data. Filled with "None".
    * Filled `LotFrontage` (street distance) using the city median.
2.  **Outlier Removal:**
    * Identified and removed huge houses (> 4000 sq ft) that were sold for abnormally low prices to prevent model skewing.
3.  **Feature Engineering:**
    * Applied **One-Hot Encoding** to convert categorical text data (e.g., "KitchenQual") into numerical binary matrices, resulting in over 300 features.
4.  **Modeling:**
    * Algorithm: **Random Forest Regressor** (Ensemble method).
    * Configuration: 100 Trees.

### 📊 Results
* **R² Score (Validation):** 89.14%
* **RMSE (Root Mean Squared Error):** ~$24,487
* **Key Insight:** The `OverallQual` (Overall Quality) feature had the highest correlation with the sale price.

---

<a name="descrição-em-português"></a>
## 🇧🇷 Descrição em Português

### Visão Geral do Projeto
Este projeto é uma solução completa de ciência de dados para a competição do Kaggle: **"House Prices - Advanced Regression Techniques"**.
O objetivo é prever o preço final de cada casa em Ames, Iowa, usando 79 variáveis explicativas. Construímos com sucesso um modelo com **~89% de precisão (Score R²)** no conjunto de validação.

### 🛠️ Técnicas e Fluxo de Trabalho
1.  **Limpeza e Imputação de Dados:**
    * Identificamos que `NaN` em colunas como `PoolQC`, `Fence` e `Alley` significavam "Ausência do item", e não dado perdido. Preenchemos com "None".
    * Preenchemos `LotFrontage` (distância da rua) usando a mediana da cidade.
2.  **Remoção de Outliers:**
    * Identificamos e removemos casas gigantes (> 4000 pés quadrados) que foram vendidas por preços anormalmente baixos para evitar distorções no modelo.
3.  **Engenharia de Atributos:**
    * Aplicamos **One-Hot Encoding** para converter dados de texto categóricos (ex: "KitchenQual") em matrizes binárias numéricas, resultando em mais de 300 colunas.
4.  **Modelagem:**
    * Algoritmo: **Random Forest Regressor** (Método Ensemble).
    * Configuração: 100 Árvores.

### 📊 Resultados
* **Score R² (Validação):** 89.14%
* **RMSE (Erro Quadrático Médio):** ~$24,487
* **Insight Principal:** A variável `OverallQual` (Qualidade Geral) apresentou a maior correlação com o preço de venda.

---

### 💻 How to Run / Como Rodar
1. Clone the repository / Clone o repositório:
   ```bash
   git clone [https://github.com/smartielo/house-prices-analysis.git](https://github.com/smartielo/house-prices-analysis.git)
   
2. Install requirements / Instale os requisitos:
   ```bash
   pip install pandas matplotlib seaborn scikit-learn

3. Run the notebook / Rode o notebook:
    ```bash
   analise_houses.ipynb
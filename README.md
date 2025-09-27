## MVP_MachineLearning-Analytics

# 📊 Previsão de Demanda de Produtos  

Este projeto tem como objetivo prever as vendas semanais de produtos a partir de dados históricos, aplicando técnicas de aprendizado de máquina e boas práticas de análise em séries temporais.  

---

## 🎯 Objetivo  
Construir modelos preditivos capazes de antecipar a demanda de produtos, comparando algoritmos clássicos e avaliando ganhos em relação a um baseline simples (**Lag-1**).  
O foco é demonstrar um **pipeline reprodutível** de previsão, desde a preparação dos dados até a avaliação final dos modelos.  

---

## 📂 Dataset  
O dataset utilizado foi obtido no **UCI Machine Learning Repository**.  
Ele contém registros de vendas semanais de múltiplos produtos, com as seguintes informações principais:  

- `date`: data da semana  
- `product_code`: código identificador do produto  
- `sales`: quantidade vendida  

---

## 🔎 Etapas Realizadas  

### 1. Análise Exploratória (EDA)  
- Tendência das vendas totais ao longo do tempo  
- Identificação dos produtos mais vendidos  
- Distribuição das vendas semanais  

### 2. Pré-Processamento  
- Criação de variáveis temporais (**lags, médias móveis, calendário**)  
- Padronização e encoding em **pipeline reprodutível**  
- Divisão temporal em **treino (70%) e teste (30%)**  

### 3. Modelagem  
- **Baseline**: Lag-1  
- **Modelos testados**:  
  - Regressão Linear  
  - Ridge  
  - Lasso  
  - SVR  
  - KNN  
  - RandomForest  
- **Otimização leve**: `RandomizedSearchCV` + `TimeSeriesSplit`  
- **Ensemble**: `VotingRegressor` com os melhores modelos  

### 4. Avaliação  
- **Métricas**: MAE, RMSE, R², MAPE, WMAPE  
- RandomForest obteve melhor desempenho:  
  - MAE ≈ **2.21**  
  - WMAPE ≈ **26%**  

---

## ✅ Conclusão  
O projeto demonstrou **ganhos significativos em relação ao baseline**, comprovando o valor da aplicação de modelos de ML em previsão de demanda.  
As técnicas implementadas garantem **reprodutibilidade** e podem ser expandidas para cenários reais, incorporando variáveis externas e modelos mais avançados.  

---

## 📌 Fonte dos Dados  
- [UCI Machine Learning Repository – Store Item Demand Forecasting Dataset](https://archive.ics.uci.edu/ml/datasets/Store+Item+Demand+Forecasting+Challenge)  


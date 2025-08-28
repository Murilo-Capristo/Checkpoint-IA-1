# ✅ Checkpoint 01 — Data Science & Machine Learning

Este repositório contém a entrega do **Checkpoint 01** da disciplina de **Data Science & ML**, com análise exploratória, modelagem e experimentos de Machine Learning aplicados a dois datasets clássicos da UCI Machine Learning Repository.

---

## 📂 Estrutura do Projeto

- `Notebook.ipynb` → Notebook principal com todas as etapas de análise, visualização e modelos.
- `README.md` → Este arquivo, com instruções e descrição detalhada do projeto.

---

## 📊 Datasets Utilizados

### 1) Individual Household Electric Power Consumption (UCI 00235)
- **Fonte:** [UCI Repository](https://archive.ics.uci.edu/ml/datasets/Individual+household+electric+power+consumption)
- **Link direto:**  
  [household_power_consumption.zip](https://archive.ics.uci.edu/ml/machine-learning-databases/00235/household_power_consumption.zip)
- **Descrição:**  
  Contém medições de potência elétrica em uma residência, coletadas a cada minuto durante quase 4 anos (2006–2010).
- **Atributos principais:**
  - `Global_active_power` (kW): potência ativa consumida (energia útil).
  - `Global_reactive_power` (kVAR): potência reativa (associada a campos elétricos/magnéticos).
  - `Voltage` (V): tensão elétrica instantânea.
  - `Global_intensity` (A): corrente elétrica.
  - `Sub_metering_1..3`: energia medida em subcircuitos específicos.
- **Pré-processamento realizado:**
  - Conversão de datas e horas para `datetime`.
  - Tratamento de valores ausentes representados como `"?"`.
  - Criação de novas variáveis (`Weekday`, `Total_Sub_metering`).
  - Agregações diárias, semanais e mensais para análise de padrões de consumo.

---

### 2) Appliances Energy Prediction (UCI 00374)
- **Fonte:** [UCI Repository](https://archive.ics.uci.edu/ml/datasets/Appliances+energy+prediction)
- **Link direto:**  
  [energydata_complete.csv](https://archive.ics.uci.edu/ml/machine-learning-databases/00374/energydata_complete.csv)
- **Descrição:**  
  Dados coletados em uma casa habitada, com sensores internos e externos, para prever consumo energético de eletrodomésticos.
- **Atributos principais:**
  - `Appliances` (Wh): consumo de energia dos eletrodomésticos (variável alvo).
  - Variáveis ambientais internas: `T1..T9` (temperaturas), `RH1..RH9` (umidade relativa).
  - Variáveis ambientais externas: `T_out`, `RH_out`, `Press_mm_hg`, `Windspeed`, `Visibility`, `Tdewpoint`.
  - `date`: timestamp.
- **Pré-processamento realizado:**
  - Conversão de `date` para `datetime`.
  - Normalização das variáveis numéricas (Min-Max Scaling).
  - Análise de distribuição e séries temporais.
  - Criação de variável binária (`alto consumo` vs `baixo consumo`) a partir da mediana de `Appliances`.

---

## 🔎 Principais Etapas Realizadas

### Parte 1 — Individual Household Electric Power Consumption
- Tratamento e exploração inicial dos dados.
- Análises de consumo diário, semanal e sazonal.
- Visualizações (séries temporais, histogramas, boxplots).
- K-Means clustering em médias diárias.
- Decomposição de séries temporais.
- Modelos de regressão linear (simples e polinomial).

### Parte 2 — Exercícios adicionais (IHEPC)
- Análise horária do consumo.
- Autocorrelação para detectar padrões diários.
- PCA para redução de dimensionalidade.
- Visualização de clusters no espaço PCA.

### Parte 3 — Appliances Energy Prediction
- Análise exploratória (EDA).
- Correlações entre variáveis ambientais e `Appliances`.
- Regressão Linear Múltipla.
- Random Forest Regressor.
- K-Means para perfis de consumo.
- Classificação binária (`alto` vs `baixo` consumo):
  - Logistic Regression.
  - Random Forest Classifier.
  - Avaliação por acurácia, precisão, recall, F1 e matriz de confusão.

---

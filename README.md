# 📊 Regression Modeling of Social Indicators
[![R](https://img.shields.io/badge/R-4.3+-blue.svg)](https://www.r-project.org/)
[![ggplot2](https://img.shields.io/badge/ggplot2-✓-orange.svg)](https://ggplot2.tidyverse.org/) [![MASS](https://img.shields.io/badge/MASS-✓-green.svg)](https://cran.r-project.org/package=MASS)
---

## 📌 Overview
This project applies **multiple regression modeling** to analyze **reported crime rates across 47 U.S. states in 1960**.

Unlike simple fixed-average approaches, our framework accounts for:
- 👦 Youth male population
- 🎓 Education levels
- 📉 Unemployment rates
- 💵 Income inequality
- 🌎 Regional differences (South vs. Non-South)

The analysis was completed as part of **ST362 – Linear Regression** at **Wilfrid Laurier University (Aug 2025)**.

---

## 👥 Team Members
- **Diya Bajaj**
- Joel Huebner

---

## ⚙️ Methodology

### 🔹 1. Exploratory Data Analysis (EDA)
- Histograms, boxplots, and correlation matrices  
- Detection of skewness & outliers  
- Southern vs. Non-Southern comparisons

### 🔹 2. Model Development
- Baseline multiple regression (**Adjusted R² = 67.6%**)  
- Stepwise **AIC model selection**  
- **Box–Cox transformation** (λ = 0.26) to address skewness  
- **Interaction models** to improve explanatory power

### 🔹 3. Classification
- Logistic regression to classify states into **high-crime vs. low-crime** groups  
- Interpreted model probabilities for policy insight

---

## 📊 Results

Key Findings:
- Adjusted R² improved from **67.6% (baseline)** → **85.6% (final interaction model)**
- Significant predictors included:
  - 👦 Youth male population (Age 14–24)
  - 🎓 Education (Ed)
  - 📉 Unemployment (U2: urban males 35–39)
  - 💵 Income inequality (X: families below ½ median income)
- Logistic regression achieved ~**78%** classification accuracy

| 📐 Metric                | 🔢 Value |
|--------------------------|--------:|
| Baseline Adj. R²         | 67.6%   |
| Final Model Adj. R²      | 85.6%   |
| Transformation           | Box–Cox (λ = 0.26) |
| Logistic Accuracy        | ~78%    |

📉 Example visualization (replace with your own plot):  
![Crime Regression Results](https://via.placeholder.com/700x300.png?text=Insert+Regression+Diagnostic+Plot)

---

## 🖥️ Code Structure

File: `crime_regression.R`

- `summary()` → descriptive statistics  
- `corrgram()` → correlation analysis  
- `lm()` → baseline regression model  
- `stepAIC()` → model selection  
- `boxcox()` → transformation  
- `glm(family = binomial)` → logistic regression

---

## 🛠️ Tech Stack
- 🐍 **R 4.3+**
- 📊 **ggplot2** – visualization
- 📈 **MASS** – Box–Cox & stepwise AIC
- 🔍 **corrgram** – correlation matrices
- 🧮 **car** – diagnostics

---


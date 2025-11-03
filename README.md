# 🌍 Life Expectancy Analysis — Health and Demographics  
**Predicting Global Life Expectancy Using Multiple Linear Regression**

![Language](https://img.shields.io/badge/Language-R-blue)
![Model](https://img.shields.io/badge/Model-Multiple%20Linear%20Regression-green)
![Dataset](https://img.shields.io/badge/Dataset-Kaggle%20Health%20%26%20Demographics-orange)
![Status](https://img.shields.io/badge/Status-Completed-success)

---

## 🎯 Problem Statement
This project investigates **which socioeconomic, health, and demographic factors influence life expectancy** across nations.  
Using global data from 2000–2015, a **multiple linear regression model** was built to identify statistically significant predictors and quantify their relationship with life expectancy.

The objective is to provide insights into **how education, healthcare, income, and disease prevalence** impact population longevity across developed and developing countries.

---

## 🧠 Dataset Overview
- **Source:** [Kaggle – Health and Demographics Dataset](https://www.kaggle.com/datasets/uom190346a/health-and-demographics-dataset)
- **Records:** 1,649 observations  
- **Variables:** 22 total (20 numerical, 2 categorical)
- **Key Features:**
  - *Economic:* GDP, Health Expenditure, Income Composition of Resources  
  - *Health:* Adult Mortality, HIV/AIDS, BMI, Immunization Coverage  
  - *Social:* Schooling, Alcohol Consumption  
  - *Target:* Life Expectancy (Years)

---

## ⚙️ Methodology

### 1️⃣ Data Preprocessing
- Cleaned missing values and standardized variable names.  
- Added **Continent** mapping using the `countrycode` library.  
- Removed non-predictive columns (`Country`, `Year`) to reduce multicollinearity.  
- Converted categorical variables into factors (`Status`, `Continent`).  
- Checked and managed multicollinearity using **Variance Inflation Factor (VIF)** analysis.

### 2️⃣ Exploratory Data Analysis (EDA)
- Conducted summary statistics and distribution checks.  
- Created **histograms**, **scatter plots**, and **boxplots** to identify relationships and outliers.  
- Observed that life expectancy correlates strongly with **GDP**, **Schooling**, and **Immunization rates**.  
- Compared developed vs. developing countries to highlight disparities in longevity.

### 3️⃣ Model Development
- Built baseline and optimized **Multiple Linear Regression (MLR)** models.  
- Applied **Stepwise Regression (Forward & Backward Elimination)** for feature selection.  
- Validated model assumptions (normality, independence, homoscedasticity).  

### 4️⃣ Model Evaluation
| Metric | Value |
|:-------|:------:|
| Adjusted R² | **0.85** |
| RMSE | **3.37** |
| Correlation (Predicted vs Actual) | **0.92** |

### 5️⃣ Advanced Regression Techniques
To reduce overfitting and handle correlated predictors:
- **Ridge Regression**
- **LASSO Regression**
- **ElasticNet Regression**

These regularization models confirmed the robustness of key predictors and improved generalization.

---

## 📊 Key Insights
- **Positive Predictors:** Schooling, GDP, Health Expenditure, Income Composition, Immunization Coverage  
- **Negative Predictors:** Adult Mortality, HIV/AIDS prevalence, Alcohol Consumption  
- Developed countries show higher life expectancy driven by **education and economic stability**.  
- Developing countries depend more on **basic healthcare access** and immunization coverage.

> ✅ Final model explains **~85% of variance** in life expectancy (Adjusted R² = 0.851).

---

## 🧾 Quantitative Highlights
- Built regression model using **R (lm)** with 12 significant predictors.  
- Verified model stability via **3-fold cross-validation** and residual diagnostics.  
- Achieved **correlation = 0.92** between predicted and actual life expectancy values.

---

## 🧩 Visual Highlights
- 📈 **Scatter Plots** – Life Expectancy vs GDP, Alcohol, Schooling  
- 🗺️ **Box Plots** – Developed vs Developing Countries  
- 🔥 **Heatmaps** – Correlation between all predictors  
- 📉 **Residual & Q–Q Plots** – Validation of model assumptions  

---

## 🚀 Tools & Technologies
**Language:** R  
**Libraries:** `dplyr`, `ggplot2`, `car`, `glmnet`, `DAAG`, `countrycode`  
**Techniques:** Multiple Linear Regression, Ridge, LASSO, ElasticNet, Cross-Validation  
**Concepts:** Feature Engineering, VIF Analysis, Model Diagnostics, Stepwise Regression

---

## 🏁 Conclusion
- The final model captures key socioeconomic and health drivers of global life expectancy.  
- Education and income distribution emerged as the strongest predictors of longer lifespan.  
- The model’s interpretability and accuracy make it suitable for **public health policy analysis**.  
- Findings align with WHO-reported global health disparities, emphasizing the importance of **education and healthcare access**.

---

## 🔮 Future Work
- Integrate **environmental and lifestyle indicators** (pollution, diet, smoking).  
- Experiment with **non-linear models** (Random Forest, XGBoost).  
- Build a **web dashboard (R Shiny)** for interactive life expectancy prediction.  

---

## 👩‍💻 Author
**Sai Raga Mounika Darimireddy**
Originally initiated as a course group project for *DS423 – Applied Data Analysis*, later **extended individually** for advanced regression modeling, diagnostics, and visualization.



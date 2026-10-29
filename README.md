# AI-Based Crude Oil Characterization and Refinery Yield Prediction

An ML-based decision-support system for predicting crude oil distillation characteristics from physicochemical properties to support preliminary refinery feedstock assessment.

## 📌 Overview

Crude oils vary in properties such as API gravity, sulfur content, nitrogen content, viscosity, and pour point. These variations influence their distillation behavior and the distribution of refinery product fractions.

This project explores the use of machine learning to learn relationships between crude oil properties and distillation profiles using historical **Crude Oil Analysis (COA)** data. The goal is to develop a data-driven tool that predicts selected distillation characteristics and presents the results through a simple interface.

## 🎯 Objectives

- Preprocess and clean historical crude oil characterization data.
- Perform exploratory data analysis and correlation analysis to identify relevant features.
- Select meaningful physicochemical properties for model development.
- Develop machine learning models to predict selected distillation fractions.
- Compare model performance using R², Mean Absolute Error (MAE), and Root Mean Squared Error (RMSE).
- Build an interactive interface for visualizing predicted fraction profiles.

## 📊 Dataset

The project uses the **Crude Oil Analysis (COA) Database**, which contains historical crude oil analyses and associated physical, chemical, and distillation properties.

Potential input features include:

- API gravity / specific gravity
- Sulfur content
- Nitrogen content
- Viscosity
- Pour point
- Other relevant physicochemical properties, depending on data availability

The target variables are selected distillation fraction characteristics.

**Data source:** [Crude Oil Analysis (COA) Database — Data.gov](https://catalog.data.gov/dataset/crude-oil-analysis-coa-database)

## ⚙️ Methodology

### 1. Data Preprocessing

- Handle missing and invalid values.
- Examine inconsistent data entries.
- Separate input properties from target variables.
- Exclude irrelevant identification and administrative fields.

### 2. Exploratory Data Analysis

- Analyze the distributions of crude oil properties.
- Examine correlations between input features and target variables.
- Identify redundant or highly correlated features.

### 3. Feature Selection

- Select chemically meaningful input variables.
- Reduce redundant features to develop a compact and interpretable feature set.

### 4. Model Development

Two regression approaches are considered:

**Linear Regression**

- Serves as an interpretable baseline model.
- Evaluates the predictive capability of linear relationships between crude oil properties and distillation characteristics.

**Random Forest Regression**

- Captures nonlinear relationships between crude oil properties and predicted distillation characteristics.
- Provides an alternative to the linear baseline for model comparison.

### 5. Model Evaluation

The models are evaluated using:

| Metric   | Purpose                                                                |
| -------- | ---------------------------------------------------------------------- |
| R² Score | Measures the proportion of variance explained by the model             |
| MAE      | Measures the average absolute prediction error                         |
| RMSE     | Measures prediction error while penalizing larger errors more strongly |

The final model is selected based on its performance on held-out test data.

### 6. Software Interface

A Streamlit-based interface is planned to allow users to:

1. Enter selected crude oil properties.
2. Generate predicted distillation fraction characteristics.
3. View the predicted fraction profile using visualizations.
4. Use the predictions as preliminary decision-support information for crude feedstock assessment.

## 🛠️ Technology Stack

The planned technology stack includes:

- **Language:** Python
- **Data Processing:** Pandas, NumPy
- **Machine Learning:** Scikit-learn
- **Visualization:** Matplotlib

## 📈 Expected Outcomes

- A cleaned dataset containing relevant crude oil properties.
- An analysis of relationships between crude oil characteristics and distillation fractions.
- Comparative evaluation of Linear Regression and Random Forest Regression.
- A selected predictive model based on test-set performance.
- An interactive interface for visualizing predicted distillation profiles.

## 👥 Project Information

- **Course:** CH330
- **Domain:** Chemical Engineering, Machine Learning, Data Analytics

---

*Turning crude-oil data into refinery intelligence.*

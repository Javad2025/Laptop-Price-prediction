# 💻 Laptop Price Prediction

## 📌 Project Overview

This project focuses on cleaning, preprocessing, and analyzing an uncleaned laptop dataset and developing a machine learning regression model to predict laptop prices based on their specifications.

The dataset contains more than 1,300 laptop product listings with information about brands, laptop types, screen specifications, processors, RAM, storage, GPUs, operating systems, weight, and price.

The main challenge of this project is that the original dataset contains various data quality issues, including missing values, inconsistent formats, mixed data types, and unstructured information. Therefore, a significant part of the project focuses on **data cleaning and feature engineering** before applying machine learning techniques.

The project follows a typical end-to-end data science workflow:

**Data Cleaning → Exploratory Data Analysis → Feature Engineering → Data Preprocessing → Model Training → Model Evaluation**

---

## 🎯 Project Objective

The main objective is to build a machine learning model that can estimate the price of a laptop based on its technical specifications.

More specifically, the project aims to:

- Clean and preprocess the raw dataset
- Identify and handle missing and inconsistent values
- Convert unstructured information into useful numerical features
- Explore relationships between laptop specifications and price
- Perform feature engineering
- Encode categorical variables
- Scale numerical features where appropriate
- Train regression models
- Evaluate model performance using appropriate regression metrics
- Identify the most important factors affecting laptop prices

---

## 📊 Dataset Summary

The dataset contains **1,300+ laptop product listings** and provides information about different laptop models and their technical specifications.

The dataset contains both **categorical** and **numerical** variables.

### Categorical Features

Examples include:

- Brand
- Laptop Type
- Screen Resolution
- CPU
- Storage Type
- GPU
- Operating System

### Numerical Features

Examples include:

- Screen Size
- RAM
- Storage Capacity
- Weight
- Price

The target variable is:

> **Price** — a continuous numerical variable representing the price of the laptop.

---

## 🧹 Data Quality Challenges

The original dataset is intentionally uncleaned and contains several data quality issues that need to be addressed before modeling.

These include:

- Missing values
- Inconsistent formatting
- Mixed data types
- Numerical values stored as strings
- Units included inside numerical columns
- Multiple pieces of information stored in a single column
- Inconsistent categorical values
- Potential outliers

For example, specifications such as CPU, storage, and screen resolution contain multiple pieces of information in a single text field.

Therefore, the preprocessing stage is an important part of this project.

---

## 🔧 Feature Engineering

One of the main goals of this project is to transform the raw laptop specifications into meaningful machine learning features.

Examples of potential feature engineering include:

- Extracting CPU brand and processor family
- Extracting CPU speed
- Converting RAM into numerical values
- Extracting storage capacity
- Separating SSD and HDD storage
- Extracting screen width and height from resolution
- Calculating total pixels
- Creating screen aspect ratio
- Extracting GPU brand
- Converting laptop weight to numerical values
- Encoding operating systems
- Encoding laptop brands and types

These transformations allow the machine learning model to work with structured numerical and categorical information rather than raw text.

---

## 📋 Column Descriptions

| Column | Description |
|---|---|
| **Brand** | The manufacturer of the laptop, such as Apple, HP, Acer, Dell, Asus, Lenovo, or Chuwi. |
| **Type** | The type of laptop, such as Ultrabook, Notebook, Gaming, or 2-in-1 Convertible. |
| **Screen Size** | The diagonal screen size measured in inches. |
| **Screen Resolution** | The display resolution of the laptop. |
| **CPU** | The processor type and speed, such as Intel Core i5 2.3GHz or AMD A9-Series 9420 3GHz. |
| **RAM** | The amount of RAM installed, measured in GB. |
| **Storage Type** | The type of storage device, such as SSD, HDD, or Flash Storage. |
| **Storage Size** | The storage capacity of the laptop. |
| **GPU** | The graphics processing unit and its specifications. |
| **Operating System** | The operating system installed on the laptop, such as Windows, macOS, or Linux. |
| **Weight** | The weight of the laptop measured in kilograms. |
| **Price** | The selling price of the laptop and the target variable for the prediction model. |

---

## 🔍 Exploratory Data Analysis

The exploratory analysis investigates the relationship between laptop specifications and prices.

Some of the questions explored include:

- Which laptop brands have the highest average prices?
- Does RAM have a strong relationship with price?
- How does storage capacity affect price?
- Are SSD laptops more expensive than HDD laptops?
- Does screen resolution influence price?
- How does CPU performance relate to price?
- Does GPU type have a significant effect on price?
- Are there significant price differences between operating systems?
- Which features have the strongest relationship with laptop price?

Visualizations are used to identify trends, distributions, relationships, and potential outliers.

---

## 🤖 Machine Learning

Since **Price** is a continuous numerical target, this project is treated as a **regression problem**.

The project starts with a simple baseline model and then evaluates more advanced approaches.

Potential models include:

- Linear Regression
- Ridge Regression
- Lasso Regression
- Random Forest Regressor
- Gradient Boosting Regressor

The models can then be compared to determine which approach provides the best predictive performance.

---

## 📏 Model Evaluation

The regression models are evaluated using several metrics:

### Mean Absolute Error (MAE)

Measures the average absolute difference between the actual and predicted prices.

\[
MAE = \frac{1}{n}\sum |y_i-\hat{y_i}|
\]

### Root Mean Squared Error (RMSE)

Penalizes larger prediction errors more strongly than MAE.

\[
RMSE = \sqrt{\frac{1}{n}\sum(y_i-\hat{y_i})^2}
\]

### R² Score

Measures how much of the variation in laptop prices is explained by the model.

\[
R^2 = 1-\frac{SS_{res}}{SS_{tot}}
\]

The final model will be evaluated using the test dataset to estimate its performance on previously unseen laptop specifications.

---

## 🛠️ Technologies & Libraries

The project is developed using Python and the following libraries:

- **Python**
- **Pandas** — Data manipulation and cleaning
- **NumPy** — Numerical computing
- **Matplotlib** — Data visualization
- **Seaborn** — Statistical visualization
- **Scikit-learn** — Machine learning and preprocessing
- **Jupyter Notebook** — Development and analysis environment

---

## 🔄 Project Workflow

```text
Raw Dataset
     ↓
Data Inspection
     ↓
Data Cleaning
     ↓
Handling Missing Values
     ↓
Handling Inconsistent Data
     ↓
Feature Engineering
     ↓
Exploratory Data Analysis
     ↓
Encoding Categorical Features
     ↓
Train/Test Split
     ↓
Feature Scaling
     ↓
Model Training
     ↓
Cross-Validation & Hyperparameter Tuning
     ↓
Model Evaluation
     ↓
Final Laptop Price Prediction

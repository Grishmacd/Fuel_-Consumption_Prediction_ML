# Fuel Consumption Prediction Using Linear Regression (Machine Learning)

This project builds a **regression** model to predict **fuel consumption (kmpl)** based on vehicle and driving factors like **engine size, vehicle weight, and speed**. It follows the standard ML workflow:

**Problem Statement → Selection of Data → Collection of Data → EDA → Train/Test Split → Model Selection → Evaluation Metric**

---

## Problem Statement
Fuel efficiency changes depending on engine capacity, vehicle load, and speed.  
The goal of this project is to predict **Fuel Consumption (kmpl)** using key inputs.

**Input Features:**
- `Engine_Size_L`
- `Weight_kg`
- `Speed_kmph`

**Output:**
- Predicted `Fuel_Consumption_kmpl`

---

## Selection of Data
**Dataset Type Used:** Structured tabular dataset (numeric features)

Why this dataset is suitable:
- Clear regression target (`Fuel_Consumption_kmpl`)
- Features are numeric and practical for prediction
- Good beginner project to understand regression and evaluation

---

## Collection of Data
In this project, the dataset is created inside the code as a sample dictionary and converted into a DataFrame using `pandas`.  
(The same workflow works with real vehicle datasets loaded using `pd.read_csv()`.)

---

## EDA (Exploratory Data Analysis)
EDA is kept simple to confirm the dataset before training:
- Confirm feature columns and target column
- Understand value ranges for engine size, weight, speed, and fuel consumption

---

## Dividing Training and Testing
The dataset is split using `train_test_split`:
- Training set: model learns relationships
- Testing set: model performance is checked on unseen data

---

## Model Selection
**Model used:** Linear Regression (`sklearn.linear_model.LinearRegression`)

Why Linear Regression:
- Simple and strong baseline for numeric regression problems
- Works well when relationships are approximately linear
- Easy to train and understand for beginners

---

## Evaluation Metric (Used in this Project)
This project uses **R² Score** (`r2_score`) to evaluate model performance.

Simple meaning:
- R² shows how well the model predictions match the real values
- Higher R² means better model fit on test data

Used in code:
- `r2_score(y_test, y_pred)`

---

## Main Libraries Used (and why)

1. `pandas`  
   - Creates and manages the dataset as a DataFrame.

2. `numpy`  
   - Supports numerical operations and array handling.

3. `sklearn.model_selection.train_test_split`  
   - Splits the dataset into training and testing sets.

4. `sklearn.linear_model.LinearRegression`  
   - Trains the regression model.

5. `sklearn.metrics.r2_score`  
   - Evaluates model performance using R² score.

---

## Output
- Printed **R² Score** for model performance
- Predicted fuel consumption for a new input (example: `[1.6, 1250, 75]`)

---

## Developer
Grishma C.D

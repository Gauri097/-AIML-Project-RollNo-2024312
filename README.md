# -AIML-Project-RollNo-2024312
Medical Insurance Cost Prediction using Linear Regression
# Medical Insurance Cost Prediction

## Problem Statement

Medical insurance charges vary depending on factors such as age, BMI, smoking habits, gender, number of children, and region. This project aims to build a Machine Learning model that predicts an individual's medical insurance charges based on these factors. The predictions can help in estimating insurance costs and understanding which factors have the greatest impact.

## Dataset

- **Name:** Medical Cost Personal Dataset
- **Source:** Kaggle
- **Link:** https://www.kaggle.com/datasets/mirichoi0218/insurance
- **Rows / Columns:** 1,338 rows and 7 columns (1,337 rows after removing one duplicate).

## Tools Used

- Python
- Pandas, NumPy
- Matplotlib, Seaborn
- Scikit-learn
- Jupyter Notebook

## Workflow

1. **Data Collection:** Downloaded the Medical Cost Personal Dataset from Kaggle.
2. **Data Cleaning:** Checked missing values, removed duplicate records, checked invalid values, and standardized categorical data.
3. **Exploratory Data Analysis (EDA):** Created graphs to study insurance charges and their relationship with different features.
4. **Feature Engineering:** Applied One-Hot Encoding to convert categorical variables into numerical form and Polynomial Features (degree 2) to capture additional relationships.
5. **Model Building:** Trained and compared Linear Regression, Log-Transformed Linear Regression, and Polynomial Linear Regression models.
6. **Evaluation:** Compared model performance using R² Score, MAE, and RMSE.
7. **Insights & Recommendations:** Studied feature importance to understand how smoking status, BMI, age, and other factors affect predictions.

## Results

- **Model:** Polynomial Linear Regression (Degree 2)
- **Key Metrics:**
  - R² Score: 0.8825
  - MAE: 2867.32
  - RMSE: 4646.06

**Model Comparison:**

| Model | R² Score | MAE | RMSE |
|---|---:|---:|---:|
| Linear Regression | 0.8069 | 4177.05 | 5956.34 |
| Log-Transformed Linear Regression | 0.7181 | 3755.92 | 7197.03 |
| Polynomial Linear Regression | **0.8825** | **2867.32** | **4646.06** |

**Top Factors / Drivers:**

- **Smoking Status:** The most important feature. Average charges were approximately 32,050 for smokers and 8,441 for non-smokers.
- **BMI:** The second most important feature. Higher BMI values were generally associated with higher insurance charges.
- **Age:** The third most important feature. Charges generally increased with age.

Permutation Importance was used to identify the most important features. These results show how much the model relies on each feature for prediction, not a cause-and-effect relationship.

## Screenshots

**1. Distribution of Insurance Charges**

![Insurance Charges Distribution](Images/charges_distribution.png)

**2. Insurance Charges by Smoking Status**

![Insurance Charges by Smoking Status](Images/charges_by_smoker.png)

**3. BMI vs Insurance Charges**

![BMI vs Insurance Charges](Images/bmi_vs_charges.png)

**4. Correlation Heatmap**

![Correlation Heatmap](Images/correlation_heatmap.png)

## Future Improvements

- Try other models such as Random Forest Regression and compare their performance.
- Use cross-validation to check how well the model performs on different data splits.
- Test the model on a larger and more diverse dataset.
- Develop a simple web application where users can enter their details and get predicted insurance charges.

## Author

**Gauri Ghansela**  
B.Sc. (Hons.) Computer Science  
University of Delhi
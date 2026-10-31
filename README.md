# -AIML-Project-RollNo-2024312
Medical Insurance Cost Prediction using Linear Regression
# Medical Insurance Cost Prediction

## 1. Problem Statement

Medical insurance charges differ from person to person based on factors such as age, BMI, smoking habits, gender, number of children, and region. Estimating these charges can be difficult because multiple factors are involved.

The objective of this project is to use Machine Learning to predict individual medical insurance charges based on these personal details.

## 2. Business Objective

The aim is to build a model that can estimate medical insurance costs using the available information about an individual. Such predictions can help insurance providers with cost estimation and help individuals understand how different factors are related to their expected insurance expenses.

## 3. Dataset

The project uses the [Medical Cost Personal Dataset from Kaggle](https://www.kaggle.com/datasets/mirichoi0218/insurance).

The dataset contains 1,338 records and 7 columns:

- `age` – Age of the individual
- `sex` – Gender
- `bmi` – Body Mass Index
- `children` – Number of children
- `smoker` – Smoking status
- `region` – Residential region
- `charges` – Medical insurance charges (target variable)

One duplicate record was removed, leaving 1,337 records for analysis.

## 4. Tools and Libraries

- Python
- Pandas and NumPy
- Matplotlib and Seaborn
- Scikit-learn
- Jupyter Notebook

## 5. Data Cleaning and Preprocessing

The following steps were performed:

- Checked the dataset for missing values.
- Removed duplicate records.
- Checked numerical columns for invalid or non-positive values.
- Standardized categorical values.
- Applied One-Hot Encoding to convert categorical features into numerical form.
- Split the data into training and testing sets in an 80:20 ratio.

## 6. Exploratory Data Analysis

Different graphs were created to understand the data and identify patterns.

**Main observations:**

- Most individuals have comparatively lower insurance charges, while a smaller number have very high charges.
- Smokers have much higher average insurance charges than non-smokers.
- BMI and age show positive relationships with insurance charges.
- Smoking status appears to have a strong association with insurance costs.

### Visualizations

**1. Distribution of Insurance Charges**

![Distribution of Insurance Charges](Images/charges_distribution.png)

**2. Insurance Charges by Smoking Status**

![Insurance Charges by Smoking Status](Images/charges_by_smoker.png)

**3. BMI vs Insurance Charges**

![BMI vs Insurance Charges](Images/bmi_vs_charges.png)

**4. Correlation Heatmap**

![Correlation Heatmap](Images/correlation_heatmap.png)

## 7. Model Building and Results

Three approaches were tested:

1. Linear Regression
2. Log-Transformed Linear Regression
3. Polynomial Linear Regression (Degree 2)

The models were evaluated using R² Score, Mean Absolute Error (MAE), and Root Mean Squared Error (RMSE).

| Model | R² Score | MAE | RMSE |
|---|---:|---:|---:|
| Linear Regression | 0.8069 | 4177.05 | 5956.34 |
| Log-Transformed Linear Regression | 0.7181 | 3755.92 | 7197.03 |
| Polynomial Linear Regression | **0.8825** | **2867.32** | **4646.06** |

Polynomial Linear Regression (Degree 2) gave the best results among the tested models. It achieved the highest R² score and the lowest MAE and RMSE, so it was selected as the final model.

## 8. Feature Impact Analysis

Permutation Importance was used to understand how much each feature contributes to the final model's predictions.

| Feature | Importance |
|---|---:|
| Smoker | 1.342751 |
| BMI | 0.205853 |
| Age | 0.155482 |
| Children | 0.010852 |
| Region – Southeast | 0.007186 |
| Region – Southwest | 0.006807 |
| Sex – Male | -0.000494 |
| Region – Northwest | -0.002852 |

**What the results show:**

- **Smoking status:** It is the most important feature. The dataset also shows a large difference in average charges: approximately 32,050 for smokers and 8,441 for non-smokers.
- **BMI:** It is the second most important feature. Higher BMI values are generally associated with higher insurance charges.
- **Age:** It is the third most important feature. Insurance charges generally tend to increase with age.
- **Children:** This feature has relatively low importance in the model.
- **Gender and Region:** These features have very low permutation importance, meaning that shuffling them had little effect on the model's R² score.

Permutation importance measures how much the model depends on a feature for prediction. It does not establish a cause-and-effect relationship. Small negative values indicate that shuffling the feature did not reduce model performance.

## 9. Conclusion

This project helped in understanding the factors related to medical insurance charges and applying Machine Learning to predict them. Among the tested models, Polynomial Linear Regression performed the best, achieving an R² score of 0.8825.

The feature analysis showed that smoking status, BMI, and age were the most important features for predicting insurance charges.

## 10. Repository Structure

```text
-AIML-Project-RollNo-2024312/
│
├── Dataset/
│   ├── insurance.csv
│   └── insurance_cleaned.csv
│
├── Notebook/
│   └── Medical_Insurance_Prediction.ipynb
│
├── Images/
│   ├── charges_distribution.png
│   ├── charges_by_smoker.png
│   ├── bmi_vs_charges.png
│   ├── correlation_heatmap.png
│   ├── actual_vs_predicted.png
│   └── residuals_vs_predicted.png
│
└── README.md
```

## Author

**Gauri Ghansela**  
B.Sc. (Hons.) Computer Science  
University of Delhi
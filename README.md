# -AIML-Project-RollNo-2024312
Medical Insurance Cost Prediction using Linear Regression
# Medical Insurance Cost Prediction

## About the Project

This project uses Machine Learning to predict medical insurance charges based on factors such as age, gender, BMI, smoking status, number of children, and region.

The main aim is to understand which factors affect insurance costs and build a model that can predict them.

## Dataset

The dataset is taken from Kaggle: [Medical Cost Personal Dataset](https://www.kaggle.com/datasets/mirichoi0218/insurance).

It contains 1,338 records and 7 columns. After removing one duplicate record, 1,337 records were used for analysis.

## Technologies Used

- Python
- Pandas and NumPy
- Matplotlib and Seaborn
- Scikit-learn
- Jupyter Notebook

## Project Steps

1. **Data Cleaning:** Checked missing values, removed duplicates, checked invalid values, and standardized categorical data.
2. **EDA:** Used graphs and statistical analysis to understand the data and find relationships between features.
3. **Preprocessing:** Converted categorical variables into numerical values using One-Hot Encoding.
4. **Model Building:** Trained and compared Linear Regression, Log-Transformed Linear Regression, and Polynomial Linear Regression models.
5. **Evaluation:** Compared the models using R² Score, MAE, and RMSE.

## Model Results

| Model | R² Score | MAE | RMSE |
|---|---:|---:|---:|
| Linear Regression | 0.8069 | 4177.05 | 5956.34 |
| Log-Transformed Regression | 0.7181 | 3755.92 | 7197.03 |
| Polynomial Regression (Degree 2) | **0.8825** | **2867.32** | **4646.06** |

Polynomial Regression gave the best results among the models tested, so it was selected as the final model.

## Feature Importance

Permutation Importance was used to check which features were most useful for prediction.

The results showed that:
- Smoking status had the highest importance.
- BMI was the second most important feature.
- Age was the third most important feature.
- Children, gender, and region had relatively lower importance.

## Conclusion

The project helped in understanding how different personal factors are related to medical insurance charges. Polynomial Regression performed better than the other tested models, achieving an R² score of 0.8825.

## Repository Structure

```text
-AIML-Project-RollNo-2024312/
│
├── Dataset/
├── Notebook/
├── Images/
└── README.md
```

## Author

**Gauri Ghansela**  
B.Sc. (Hons.) Computer Science  
University of Delhi
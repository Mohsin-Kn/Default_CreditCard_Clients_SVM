
# Default of Credit Card Clients using SVM

## Overview

 **Support Vector Machine (SVM)** model to predict credit card defaults using the **Default of Credit Card Clients** dataset. The dataset contains client characteristics, payment history, and credit default information.

## Dataset

-   **Source**: [UCI Machine Learning Repository](http://archive.ics.uci.edu/dataset/350/default+of+credit+card+clients)
-   **Features**:
    -   **LIMIT_BAL**: Credit limit
    -   **SEX**: Gender (1 = Male, 2 = Female)
    -   **EDUCATION**: Education level (1 = Graduate school, 2 = University, 3 = High school, 4 = Others)
    -   **MARRIAGE**: Marital status (1 = Married, 2 = Single, 3 = Others)
    -   **AGE**: Client age
    -   **PAY_0 to PAY_6**: Payment status over six months
    -   **BILL_AMT1 to BILL_AMT6**: Bill statement amounts
    -   **PAY_AMT1 to PAY_AMT6**: Amount paid in the last six months
    -   **default payment next month**: Target variable (1 = Default, 0 = No Default)

## Preprocessing Steps

Before training the SVM model, the dataset undergoes the following steps:

1.  **Data Cleaning**: Handling missing values and removing outliers.
2.  **Feature Engineering**:
    -   Dropping unnecessary columns (e.g., `ID`).
    -   Handling categorical variables via **One-Hot Encoding**.
3.  **Resampling**: Addressing class imbalance using **downsampling**.
4.  **Feature Scaling**: Standardizing numerical features.
5.  **Train-Test Split**: Splitting the dataset for model training and evaluation.

## Model Training

-   The **SVM model** is trained using `sklearn.svm.SVC()`.
-   Hyperparameter tuning is performed using **GridSearchCV**.
-   The best model is evaluated using a **confusion matrix**.


## Results

-   The model performance is evaluated using accuracy and confusion matrix.
-   Hyperparameter tuning improves performance by selecting the best `C` and `gamma` values.



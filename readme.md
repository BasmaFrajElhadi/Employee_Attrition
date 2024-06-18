# Employee Attrition Analysis

## Overview

This project analyzes employee attrition using a dataset from Kaggle. The aim is to understand the factors contributing to employee turnover and develop strategies to improve employee retention.

## Dataset

The dataset used in this project can be found on Kaggle: [Employee Attrition Dataset](https://www.kaggle.com/datasets/patelprashant/employee-attrition)

## Project Structure

- `employee_attrition_train.csv`: The main dataset file.
- `employee_attrition_analysis.ipynb`: Jupyter Notebook containing the analysis and visualization code.
- `README.md`: Project overview and documentation.

## Setup and Installation

1. **Clone the Repository:**
    ```sh
    git clone https://github.com/BasmaFrajElhadi/Employee_Attrition
    cd Employee_Attrition
    ```

2. **Install Dependencies:**
    ```sh
    pip install -r requirements.txt
    ```

## Data Preprocessing

1. **Remove Unnecessary Columns:**
    - `EmployeeCount`: Same value for all rows.
    - `StandardHours`: Same value for all rows.
    - `EmployeeNumber`: Unique identifier for each row, not useful for analysis.
    - `Over18`: Same value for all rows.

2. **Handle Missing Values:**
    - Drop rows with missing values.

3. **Encode Categorical Variables:**
    - Convert categorical columns to numerical using appropriate encoding techniques.

4. **Balance Target Variable:**
    - Use over-sampling to resolve class imbalance in the target variable (`Attrition`).

## Exploratory Data Analysis (EDA)

### Key Findings:

1. **Monthly Income vs. Attrition:**
    - Employees with higher incomes are less likely to leave the company, but high-income outliers also leave, indicating salary is not the sole factor.

2. **Hourly Rate vs. Attrition:**
    - No significant relationship between hourly rate and attrition.

3. **Salary Hike vs. Training Times Last Year:**
    - No significant effect on the number of training hours with an increase in salary.

4. **Salary Hike vs. Performance Rating:**
    - Higher salary increases are associated with higher performance ratings.

5. **Salary Hike vs. Overtime:**
    - Employees working more overtime receive smaller salary increases, which can lead to dissatisfaction.

6. **Work-Life Balance vs. Attrition:**
    - Work-life balance has a small effect on attrition.

7. **Marital Status vs. Attrition:**
    - Single employees are more likely to leave.

8. **Distance from Home vs. Work-Life Balance:**
    - Distance from home alone might not be a strong predictor of attrition.

9. **Job Satisfaction vs. Attrition:**
    - Lower job satisfaction (less than 3) is associated with higher attrition.

10. **Years Since Last Promotion vs. Attrition:**
    - Lack of recent promotion (within 0-5 years) is a factor in attrition.

11. **Training Times Last Year vs. Attrition:**
    - Minimal training is common among those who left, but high levels of training do not necessarily prevent attrition.

12. **Job Level vs. Attrition:**
    - Higher job levels have a greater chance of retaining employees, though some high-level employees still leave.

13. **Relationship Satisfaction vs. Attrition:**
    - No significant effect.

14. **Environment Satisfaction vs. Attrition:**
    - Slight effect of the environment on staying at work.

15. **Gender vs. Attrition:**
    - No significant effect of gender on attrition.

16. **Overtime vs. Attrition:**
    - Employees working overtime are more likely to leave.

17. **Job Role vs. Attrition:**
    - Research-related roles have lower attrition rates.

## Model Training and Evaluation

1. **Split Dataset:**
    - Train-Test split with 80-20 ratio.

2. **Scale Features:**
    - Standardize the features using `StandardScaler`.

3. **Train Model:**
    - Gradient Boosting Classifier with 200 estimators.

4. **Evaluate Model:**
    - Accuracy on training set: `0.996135265700483`
    - Accuracy on test set: `0.9498069498069498`

    ```plaintext
    Confusion Matrix:
    [[115   8]
    [ 5 131]]

    Classification Report:
                  precision    recall  f1-score   support

                0          0.96      0.93      0.95       123
                1          0.94      0.96      0.95       136

        accuracy                               0.95       259
        macro avg          0.95      0.95      0.95       259
        weighted avg       0.95      0.95      0.95       259

    ```

## Conclusion

### Key Takeaways:

1. **Compensation:** Competitive and fair compensation is crucial for retaining employees.
2. **Job Satisfaction:** Higher job satisfaction reduces attrition rates.
3. **Promotions:** Regular promotions are important to keep employees motivated and reduce turnover.
4. **Training:** Adequate training opportunities are essential, though they do not guarantee retention.
5. **Overtime:** Employees working excessive overtime are more likely to leave, indicating a need for better work-life balance policies.

## Future Work

1. **More Advanced Models:** Explore other machine learning models and techniques to improve prediction accuracy.
2. **Feature Engineering:** Investigate additional features and their interactions to enhance the analysis.
3. **Employee Feedback:** Incorporate qualitative data from employee feedback surveys for a more comprehensive analysis.

## References

- Kaggle Dataset: [Employee Attrition Dataset](https://www.kaggle.com/datasets/patelprashant/employee-attrition)

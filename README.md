
# Employee Performance Prediction: Resigned or Not

## Project Overview

This project aims to predict whether an employee is likely to resign based on various job-related and demographic factors. Using machine learning models, we analyze the dataset to create a predictive model that helps HR departments take proactive measures for employee retention.

## Dataset

The dataset used in this project contains the following features:

- **Department**: Department the employee works in
- **Gender**: Gender of the employee
- **Age**: Age of the employee (Selected)
- **Job_Title**: Position held by the employee
- **Years_At_Company**: Number of years the employee has worked for the company
- **Education_Level**: Education level of the employee
- **Performance_Score**: Performance rating of the employee
- **Monthly_Salary**: Employee’s monthly salary (Selected)
- **Work_Hours_Per_Week**: Number of hours the employee works per week (Selected)
- **Projects_Handled**: Number of projects handled by the employee (Selected)
- **Overtime_Hours**: Overtime hours worked by the employee (Selected)
- **Sick_Days**: Number of sick days taken by the employee
- **Remote_Work_Frequency**: Frequency of remote work
- **Team_Size**: Size of the team the employee works in (Selected)
- **Training_Hours**: Number of hours of training received by the employee (Selected)
- **Promotions**: Whether the employee has been promoted or not
- **Employee_Satisfaction_Score**: Employee's satisfaction score (Selected)
- **Resigned**: Target variable (Yes/No) indicating if the employee has resigned or not

*Note: The `Employee_ID` feature was excluded as it was not used in model training.*

### Feature Selection

The following features were selected based on their importance in predicting employee resignation:

- **Age**
- **Monthly_Salary**
- **Work_Hours_Per_Week**
- **Projects_Handled**
- **Overtime_Hours**
- **Team_Size**
- **Training_Hours**
- **Employee_Satisfaction_Score**

## Project Workflow

1. **Data Preprocessing**:
   - Handled missing data
   - Encoded categorical variables
   - Scaled numerical features
   - Addressed class imbalance using the **Random Oversampler** from the `imbalanced-learn` library.

2. **Exploratory Data Analysis (EDA)**:
   - Visualized data distributions and relationships
   - Analyzed correlations between features and the target variable

3. **Modeling**:
   Several models were tested in this project:
   - **Logistic Regression**
   - **Support Vector System**
   - **K-Nearest Neighbors (KNN)**
   - **Naive Bayes**
   - **Random Forest** (excluded due to overfitting concerns)
   - **Decision Tree** (Final Model)

   The **Decision Tree** was chosen as the final model due to its balanced performance and generalizability. **Cross-validation** was also used to ensure that the model generalizes well to unseen data.

5. **Evaluation**:
   - Metrics used to evaluate models:
     - Accuracy
     - Precision
     - Recall
     - F1 Score

   - The **Decision Tree** model showed reliable performance, with cross-validation scores ranging from **0.9339** to **0.9408**. This indicates that the model generalizes well across different subsets of the data.

## Tools & Libraries Used

- **Python**: Main programming language
- **Pandas**: For data manipulation
- **NumPy**: For numerical operations
- **Scikit-learn**: For building and evaluating machine learning models
- **Imbalanced-learn**: For handling class imbalance (Random Oversampler)
- **Matplotlib/Seaborn**: For data visualization

## How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/reddy331/Employee-Performance-Prediction-Resigned-or-Not.git
   ```

2. Install the required libraries:
   ```bash
   pip install -r requirements.txt
   ```

3. Run the Jupyter Notebook to explore the project:
   ```bash
   jupyter notebook Employee Performance Prediction(Resigned or Not).ipynb
   ```

## Conclusion

The Decision Tree model, using cross-validation and Random Oversampler for handling class imbalance, achieved promising results, demonstrating strong generalization capability. Cross-validation scores between **0.9339** and **0.9408** confirm the model's reliability. Further improvements can be made by experimenting with additional features or more complex models.

## Future Work

- Experiment with deep learning models for improved accuracy.
- Explore additional features such as employee satisfaction scores, training hours, and more job-related factors to further refine the model.

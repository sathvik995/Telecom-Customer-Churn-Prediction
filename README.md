# Telecom Customer Churn Detection

This project aims to predict customer churn, which refers to the likelihood of customers discontinuing their services. By accurately predicting churn, businesses can take proactive steps to retain customers and improve their overall satisfaction.

## Project Overview

Customer churn detection is critical for businesses looking to maintain a stable and growing customer base. This project leverages machine learning algorithms to analyze customer data and predict which customers are at risk of churning.

## Dataset Details

| Variable          | Description                                                            |
|-------------------|------------------------------------------------------------------------|
| CustomerID        | Unique customer ID                                                     |
| Gender            | Customer's gender                                                      |
| SeniorCitizen     | Whether the customer is a senior citizen or not (1, 0)                 |
| Partner           | Whether the customer has a partner or not (Yes, No)                    |
| Dependents        | Whether the customer has dependents or not (Yes, No)                   |
| Tenure            | Number of months the customer has stayed with the company              |
| PhoneService      | Whether the customer has a phone service or not (Yes, No)              |
| MultipleLines     | Whether the customer has multiple lines or not (Yes, No, No phone service) |
| InternetService   | Customer’s internet service provider (DSL, Fiber optic, No)            |
| OnlineSecurity    | Whether the customer has online security or not (Yes, No, No internet service) |
| OnlineBackup      | Whether the customer has online backup or not (Yes, No, No internet service) |
| DeviceProtection  | Whether the customer has device protection or not (Yes, No, No internet service) |
| TechSupport       | Whether the customer has tech support or not (Yes, No, No internet service) |
| StreamingTV       | Whether the customer has streaming TV or not (Yes, No, No internet service) |
| StreamingMovies   | Whether the customer has streaming movies or not (Yes, No, No internet service) |
| Contract          | The contract term of the customer (Month-to-month, One year, Two year) |
| PaperlessBilling  | Whether the customer has paperless billing or not (Yes, No)            |
| PaymentMethod     | The customer’s payment method (Electronic check, Mailed check, Bank transfer (automatic), Credit card (automatic)) |
| MonthlyCharges    | The amount charged to the customer monthly                             |
| TotalCharges      | The total amount charged to the customer                               |
| Churn             | Whether the customer churned or not (Yes or No)                        |

## Project Pipeline

The steps involved in the machine learning pipeline are:

1. **Import necessary dependencies**: Load the required libraries and modules.
2. **Read and load the dataset**: Import the dataset into the environment.
3. **Exploratory Data Analysis (EDA)**: Analyze and visualize the data to understand patterns and correlations.
4. **Data Preprocessing**: Clean and prepare the data for modeling by handling missing values, encoding categorical variables, and scaling numerical features.
5. **Splitting data**: Divide the dataset into training and testing sets.
6. **Model Building**: Train machine learning models on the training data.
7. **Model Evaluation**: Evaluate the models using appropriate metrics to select the best-performing model.

## Model Evaluation

### Metrics
- **Accuracy**: Measures the proportion of correctly predicted churn cases.
- **Precision**: Indicates the accuracy of positive predictions.
- **Recall**: Measures the ability to identify actual churn cases.
- **F1-score**: Harmonic mean of precision and recall.
- **ROC-AUC**: Evaluates the model's ability to distinguish between classes.

### Conclusion
From the exploratory data analysis, I came to know that, the senior citizens have lower churn count whereas the customers who are single or don't have dependents ahve higher churn count. In addition to that, customers are more satified with the streaming services than other services such as Online backup and Device protection, which has resulted in lower churn count in customer with streaing services than the other services.

The tenure have an inverse relation with churn count, where customer with tenure shorter than 5 months have higher churn count. Moreover, the customers with month-to-month contract have higher churn count as compared to those with one or two year contract which also proves that customer who have longer contract with the company have lower churn count.

It has been observed that the customers with higher monthly charges and lower total charges have higher churn count. Therefore, the company should focus on lowering the monthly charges for the customers in order to reduce the churn count. From the feature importance, it is clear that the tenure, contract, monthly charges, and total charges are the most important features for predicting the customer churn. Therefore, the company should focus on these features to reduce the customer churn.

Coming to the machine learning models, I have used three models - Decision Tree Classifier, Random Forest Classifier, and K Nearest Neighbors Classifier. The Random Forest Classifier has the highest accuracy i.e. 82% and F1 Score, and lowest mean squared error, mean absolute error. Therefore, the Random Forest Classifier is a good fit for predicting the customer churn.


## Key Takeaways

- **Customer churn detection** helps businesses retain customers by identifying those at risk of leaving.
- **Machine learning algorithms** such as Logistic Regression, Decision Trees, and Random Forests are effective for predicting churn.
- **Data preprocessing and feature engineering** are crucial for improving model performance.

By implementing customer churn detection, businesses can take targeted actions to improve customer retention and enhance overall customer experience.

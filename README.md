# Customer Churn Prediction in Wiretel

![Wiretel](https://example.com/wiretel_logo.png)

## Background

The telecom industry faces a significant challenge with customer churn, where customers leave one company for another. Churn rates have a profound impact on customer lifetime value and company revenue. For instance, a company with a 20% churn rate annually has an average customer lifetime of 4 years, while a company with a 50% churn rate has an average customer lifetime of 2 years. In India, the telecom sector's annual churn rate is estimated to be around 25% [1]. Churn not only results in the loss of future revenue but also erodes profitability, as acquiring new customers is expensive.

The goal of this project is to identify patterns in the data that may help reduce the proportion of churners in Wiretel, a telecom company. The dataset contains information about 3333 customers, including 20 predictors, such as account length, international plan, voice mail plan, call duration, and more.

## Dataset

The dataset contains the following fields:

- State: Categorical, representing the 50 states and the District of Columbia.
- Account length: Integer-valued, indicating how long the account has been active.
- Area code: Categorical, representing the area code associated with the customer's phone number.
- Phone number: A surrogate for customer ID, to be dropped during analysis.
- International plan: Dichotomous categorical, indicating if the customer has an international plan (yes or no).
- Voice mail plan: Dichotomous categorical, indicating if the customer has a voice mail plan (yes or no).
- Number of voice mail messages: Integer-valued, showing the number of voice mail messages.
- Total day minutes: Continuous, representing the number of minutes the customer used the service during the day.
- Total day calls: Integer-valued, indicating the number of calls made during the day.
- Total day charge: Continuous, derived from the above two variables.
- Total eve minutes: Continuous, representing the number of minutes the customer used the service during the evening.
- Total eve calls: Integer-valued, indicating the number of calls made during the evening.
- Total eve charge: Continuous, derived from the above two variables.
- Total night minutes: Continuous, representing the number of minutes the customer used the service during the night.
- Total night calls: Integer-valued, indicating the number of calls made during the night.
- Total night charge: Continuous, derived from the above two variables.
- Total international minutes: Continuous, representing the number of minutes the customer used for international calls.
- Total international calls: Integer-valued, indicating the number of international calls made.
- Total international charge: Continuous, derived from the above two variables.
- Number of calls to customer service: Integer-valued, indicating the number of calls made to customer service.
- Churn: Target variable, indicating whether the customer churned (left the company) or not.

## Data Exploration and Analysis

We start by exploring the dataset through various exploratory data analysis (EDA) techniques, such as visualizations and summary statistics. Key insights include:

- The dataset is imbalanced, with approximately 85.5% non-churners and 14.5% churners.
- Customers with international plans are more likely to churn.
- Customers who call customer service more than four times are more likely to churn.
- Customers with higher day charges are more likely to churn.

## Model Generation

Next, we proceed to build predictive models to identify factors that contribute to customer churn. We consider the following classification algorithms:

1. Decision Tree Classifier
2. Random Forest Classifier
3. Logistic Regression
4. K-Neighbors Classifier
5. Support Vector Machine (SVM)

To address the class imbalance issue, we apply the Synthetic Minority Over-sampling Technique (SMOTE) combined with Edited Nearest Neighbors (ENN) to balance the dataset before model training.

### Model Performance

We evaluate each model's performance using accuracy as the primary metric. The accuracy is calculated on both the original and balanced datasets. The models' performance can be visualized in the following table:

| Model                     | Accuracy (%) |
|---------------------------|--------------|
| Decision Tree             | 94.07        |
| Decision Tree (SMOTE)     | 85.30        |
| Random Forest             | 90.00        |
| Random Forest (SMOTE)     | 83.03        |
| Logistic Regression       | 88.00        |
| Logistic Regression (SMOTE) | 71.10       |
| K-Neighbors Classifier    | 89.00        |
| K-Neighbors Classifier (SMOTE) | 93.22    |
| Support Vector Machine    | 88.40        |
| Support Vector Machine (SMOTE) | 90.74    |


### Conclusion and Recommendations

Based on the analysis, we provide recommendations to the top management team of Wiretel to reduce customer churn:

1. Implement strategies to retain customers with international plans, as they are more likely to churn.
2. Address the concerns of customers who frequently call customer service, as they are at a higher risk of churn.
3. Focus on providing incentives and offers to customers with high day charges, as they are also prone to churn.

By leveraging these insights, Wiretel can draft a more focused retention strategy to enhance customer satisfaction and reduce churn, ultimately leading to improved long-term profitability.

---
*As an aspiring data scientist, I created this project to showcase my skills in data exploration, analysis, and predictive modeling. If you have any suggestions or feedback, feel free to reach out. Let's make data-driven decisions together!*

*Note: The datasets and codes used in this project are available in the repository. Please refer to the respective Python files for detailed code implementation.*

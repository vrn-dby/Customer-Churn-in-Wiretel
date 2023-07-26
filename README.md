# Customer Churn Prediction in Wiretel

## Background
The telecom industry faces a common challenge known as customer churn, where customers leave one company in favor of another. Churn rate significantly impacts the lifetime value of a customer and, subsequently, the company's future revenue. For instance, a 20% churn rate corresponds to an average customer lifetime of 4 years, while a 50% churn rate means an average customer lifetime of 2 years. In the Indian telecom sector, the annual churn rate is estimated to be around 25% [1]. Customer churn leads to not only lost future revenue but also the resources spent on customer acquisition, negatively affecting profitability. The objective of this project is to identify patterns in the data that can help reduce the proportion of churners in Wiretel, a telecom company.

## Dataset
The dataset contains information about 3333 customers of Wiretel, including 20 predictors and the target variable, churn, indicating whether a customer left the company or not. The dataset fields include:
- State: Categorical, representing the 50 states and the District of Columbia.
- Account length: Integer-valued, indicating the duration of the customer's active account.
- Area code: Categorical, representing the area code associated with the customer's phone number.
- Phone number: A unique identifier for each customer (surrogate for customer ID).
- International plan: Dichotomous categorical, indicating whether the customer has an international plan (yes or no).
- Voice mail plan: Dichotomous categorical, indicating whether the customer has a voicemail plan (yes or no).
- Number of voice mail messages: Integer-valued, representing the number of voicemail messages.
- Total day minutes: Continuous, indicating the minutes the customer used service during the day.
- Total day calls: Integer-valued, representing the total number of calls made during the day.
- Total day charge: Continuous, possibly derived from the total day minutes and total day calls.
- Total evening minutes: Continuous, indicating the minutes the customer used service during the evening.
- Total evening calls: Integer-valued, representing the total number of calls made during the evening.
- Total evening charge: Continuous, possibly derived from the total evening minutes and total evening calls.
- Total night minutes: Continuous, indicating the minutes the customer used service during the night.
- Total night calls: Integer-valued, representing the total number of calls made during the night.
- Total night charge: Continuous, possibly derived from the total night minutes and total night calls.
- Total international minutes: Continuous, indicating the minutes the customer used for international calls.
- Total international calls: Integer-valued, representing the total number of international calls made.
- Total international charge: Continuous, possibly derived from the total international minutes and total international calls.
- Number of calls to customer service: Integer-valued, indicating the number of calls made to customer service.
- Churn: Target variable, indicating whether the customer has left the company (True or False).

## Project Objective
The primary objective of this project is to understand the factors that explain customer churn in Wiretel. By analyzing the data, we aim to identify insights that can suggest reasons behind customer churn and draft a more focused retention strategy for the top management team of Wiretel.

## Code Description
The project includes two Python files:
1. `EDA.py`: This file contains the exploratory data analysis (EDA) phase of the project, where we visualize and analyze the data to gain insights into customer churn patterns.
2. `Model.py`: This file includes the development and evaluation of the churn prediction model using machine learning techniques.

## Approach
1. We started by loading the dataset and performing basic data exploration to understand its structure, dimensions, and data types.
2. Next, we visualized the distribution of individual predictors concerning churn to identify potential patterns and relationships.
3. We addressed data cleaning tasks, such as converting charges to numeric amounts and transforming categorical variables to binary.
4. To handle class imbalance in the target variable, we either upsampled or downsampled the data.
5. We then conducted in-depth univariate analysis to uncover factors that might contribute to churn.
6. By computing the correlation matrix, we identified correlations between predictors and the target variable.
7. Finally, we converted categorical variables into dummy variables (one-hot encoding) for model training.

## Conclusion
Through our exploratory analysis, we found several insights that can help in understanding customer churn in Wiretel. For instance, customers who call customer service more than four times and those with high day charges are more likely to churn. Additionally, customers with an international plan also exhibit a higher churn rate. Armed with these insights, we can make recommendations to the top management team of Wiretel to improve customer retention strategies and mitigate churn.

## Future Work
- Implement advanced machine learning models for churn prediction and compare their performance.
- Conduct a cost-benefit analysis to estimate the potential impact of different retention strategies.
- Deploy the churn prediction model in a real-world setting to enable proactive retention efforts.

[1] http://shodhganga.inflibnet.ac.in/bitstream/10603/31192/2/chpt%201.pdf

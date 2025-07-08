# Maximizing-Revenue-for-Drivers

## Business Problem

In the competitive taxi industry, optimizing revenue streams is essential for long-term success and driver satisfaction. With the advent of digital payments, understanding how payment methods impact fare pricing has become increasingly important for maximizing earnings.

This research focuses on leveraging data-driven insights to determine whether there is a significant relationship between the total fare amount and payment type, and if duration of the trips have any affect on fare amount. By analyzing the connection between payment methods (e.g., cash versus credit cards) and fare pricing, we aim to uncover actionable strategies for increasing driver revenue.


## Objective
The primary goal of this project is to conduct a hypothesis test to examine whether the method of payment influences total fare amounts, and regression analysis to predict whether trip duration affects fare amounts. Using Python for hypothesis testing, descriptive statistics, and linear regression, we aim to answer the following:

Are customers who pay via credit cards associated with higher fare amounts compared to those paying with cash?

Does trip duration influence fare amounts?

Can insights from payment trends guide strategies for encouraging higher-revenue payment methods without impacting customer satisfaction?

##  Tools & Technologies

'Python'

Libraries - `pandas`, `matplotlib`, `seaborn`, `scipy`, `statsmodel`, `sklearn`

## Research Question
Does the method of payment have a significant impact on the total fare amount?

By answering this question, we aim to provide practical recommendations to taxi drivers and operators on how to align payment policies with revenue optimization.

## Data Overview -
For this analysis, we utilized the comprehensive dataset of NYC Taxi Trip records, used data cleaning and feature engineering procedures to concentrate solely on the relevant columns essential for our investigation.

Relevant columns used for this research :
- passenger_count (1 to 5)
- payment_type (card or cash)
- fare_amount
- trip_distance (miles)
- duration (minutes)
![image](https://github.com/user-attachments/assets/a36f471d-2997-49ba-9a19-14c6a7e5b9c4)

## Methodology - 

Descriptive analysis : performed statistical analysis to summarize key aspects of the data, focusing on fare amounts and payment types.

Hypothesis Testing - Conducted a T-test to evaluate the relationship between payment type and fare amount, testing the hypothesis that different payment methods influence fare amounts

Regression Analysis : Implemented linear regression to explore the relationship between trip duration (calculated from pick up and drop off times) and fare amount.

## Exploratory Data Analysis
In this section, we explored the dataset to understand its structure and key attributes. The main goals of EDA are:

Assess the completeness and cleanliness of the dataset.
Analyze distributions of important features such as trip_distance, fare_amount, and pickup_datetime.
Identify patterns or anomalies that might influence revenue.

We clean the data-
 - changing datatypes
- removing null values
- removing duplicates
- removing unnecessary columns and data
- Removing Outliers 

## Journey Insights - 

- Customers paying with cards tend to have a slightly higher average trip distance and fare amount compared to those paying with cash.
- Indicates that customers prefers to pay more with cards when they have high fare amount and long trip distance.

![image](https://github.com/user-attachments/assets/bef8c69e-8da2-45ee-ab1f-f61c4415bebe)
![image](https://github.com/user-attachments/assets/b9bf1285-b379-455c-bb2e-ac6966a0fe42)

## Preference of Payment Types
- The proportion of customers paying with cards is significantly higher than those paying with cash, with card payments accounting for 67.5% of all transactions compared to cash payments at 32.5%.
- This indicates a strong preference among customers for using card payments over cash, potentially due to convenience, security, or incentives offered for card transactions.
![image](https://github.com/user-attachments/assets/ed541660-fe1e-4348-8d25-7e4fb66cc80e)

## Passenger Count Analysis
Among card payments, rides with a single passenger (passenger_count = 1) comprise the largest proportion, constituting 40.08% of all card transactions.
Similarly, cash payments are predominantly associated with single-passenger rides, making up 20.04% of all cash transactions.
- There is a noticeable decrease in the percentage of transactions as the passenger count increases, suggesting that larger groups are less likely to use taxis or may opt for alternative payment methods.
- These insights emphasize the importance of considering both payment method and passenger count when analyzing transaction data, as they provide valuable insights into customer behavior and preferences.

![image](https://github.com/user-attachments/assets/3d7fa4fe-259a-42ae-b98b-ee3582b30271)

## Hypothesis Testing

**Null hypothesis:** There is no difference in average fare between customers who use credit cards and customers who use cash.

**Alternative hypothesis:** There is a difference in average fare between customers who use credit cards and customers who use cash

With a T-statistic of 165.5 and a P-value of less than 0.05, we reject the null hypothesis, suggesting that there is indeed a significant difference in average fare between the two payment methods.
![image](https://github.com/user-attachments/assets/5b601a51-64ac-49fa-a07a-b7ca475c0987)

## Linear Regression

Train MSE: 144.77262390371942, Test MSE: 141.78242524104948
Train R²: 0.020235411107627943, Test R²: 0.017485593657060927

1. **MSE results**

    - The Train and Test MSE values are relatively close, suggesting that the model has similar performance on both datasets and is not overfitting or underfitting.
    - However, the values themselves are quite high, implying that the model's predictions are not very close to the actual values.

2. **R squared results**

    - the 𝑅 squared values for both Train and Test datasets are extremely low (~2% and ~1.7%), suggesting that trip duration has minimal explanatory power for predicting fare amount in your data.
  
**Conclusion:**

- The very low 𝑅 squared values suggest that trip duration alone is not a strong predictor of fare amount.
- The close Train and Test MSE values indicate that the model generalizes similarly on unseen data, even though the predictions are not highly accurate.

![image](https://github.com/user-attachments/assets/a381dcc5-2697-4cc2-954d-e11f658361e0)

## Recommendations

- Encourage customers to pay with credit cards to capitalize on the potential for generating more revenue for taxi cab drivers
- Implement strategies such as incentives or discounts for credit card transactions to incentivize customers to choose this payment method
- Provide seamless and secure credit card payment options to enhance customer convenience and encourage adoption of this preferred payment method.
- Focus on shorter, frequent trips during peak hours for optimal earnings.
- Explore popular routes and zones (e.g., airports or downtown areas) with high trip density. 


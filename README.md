# Project-4 Exploratory Data Analysis of Food Deliveries and Forecasting Demand

The context of this problem is you have a client from a food delivery company that operates in multiple cities. The client replenishes their food inventory on a weekly basis, and since this is perishable, the replenishment is of utmost importance. The client has given you their data on all their food deliveries for Weeks 1-145, and they want you to forecast the demand food deliveries for the next 10 weeks (Weeks 146-155). 

The dataset for this project is from Kaggle: https://www.kaggle.com/ghoshsaptarshi/av-genpact-hack-dec2018

## Project at a glance:
Code used: Python, Matplotlib, Seaborn, Pandas, Numpy, Scikit Learn

## Data Exploration:
Listed below are some of the most important insights from the dataset:
1. Checkout and base price are negatively correlated with the number of orders. There were orders that were sold at a higher checkout price vs base price and so these did not perform well.
2. The area of operations are positively correlated with the number of orders.
3. The Indian cuisine deliveries had the highest average number of orders.
4. Majority of the orders did not have an email promotion and were not featured on the company's homepage, but the items that did HAVE an email promotion or were featured on the homepage had a HIGHER average number of orders.
5. The top four most popular food deliveries are rice bowls, sandwiches, beverages, and salads.

## Machine Learning:
I split the data set into 80% for training the model and 20% for testing the model.
Models used:
1. Ridge Regression
2. Elastic Net
3. Linear Support Vector Machine
4. XGBoost Regression

### Evaluation:
I used the Root Mean Squared Error to evaluate the model performance:
| Model          | Root Mean Squared Error | 
|----------------|-------------------------|
|Ridge Reg       |    285.5547913880647    |
|Elastic Net Reg |    321.18917750771146   | 
|Linear SVM      |    313.59953782203337   |
|XGBoost Reg     |    166.63175507981836   |

Based on the results, the XGBoost model was chosen to forecast demand on the data for the next 10 weeks.

## Forecasted Deliveries for Weeks 146-155:
![Image](https://github.com/rafationgson/Project-4/blob/master/Food-Delivery-Forecast.png)

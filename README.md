# Pipeline 

# 1) Define and understand the problem 

## 1.a) What is the problem 
American express is the world's largest payment card issuer. In North America, credit card can be used daily by developing a **loan** for each purchase. The aim of this competition is to predict whether a customer should have a credit card or not therefore whether a given customer would be able to pay back the loaned money or not. It's a **binary classification** problem. To solve the problem, **time series** data are provided. 
## 1.b) Why does the problem need to be solved ? 
The reason is obvious. It's to optimize lending decisions to help them choose the best customers to avoid loosing money with "non-able to pay-back" customers. 

## 1.c) How would I solve the problem ? 
Data is provided for ananymised customers. 

# 2) Understand the metric and the submission
## 2.a) Understand the metric
To evaluate the different models, the metric used is the mean of two measures : 
- Normalized Gini coefficient **G**
- Default rate captured at 4% **D**
- $M = \frac{G + D}{2}$
- For both G and D, the negative labels are given a weight of **20** to adjust for downsampling meaning that every customer which is labeled as 0 (wouldn't be able to pay back), a weight of 20 will be assigned. 

### i) Normalized Gini coefficient 
The Gini coefficient a single number that deminstrates a degree of inequality in a distribution of income/wealth. It is used to estimate how far a country's wealth or income distribution deviates from a totally equal distribution. The lowest the Gini coefficient, the higest the equality ie in terms of ML, **the lowest G, the better the model predicts**.
Ref: https://en.wikipedia.org/wiki/Gini_coefficient#Calculation 

### ii) Default rate captured at 4% 
The default rate capture at 4% is the percentage of the positive labels (defaults) captured within the **highest-ranked 4%** of the predictions meaning this metric will keep the customers which probability of paying back (labeled as 1) is within the top 4%.

### iii) Combination of both 
Overall, **the bigger the metric M, the better the model performance**.

## 2.b) Understand the submission 
We must submit a .csv file with **924 621** predictions of the target varibale meaning the probability of a customer to belong to its label (0 or 1).

# 3) Find how the dataset was splitted into train and test 

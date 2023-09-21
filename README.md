# food-sales-predictions
The main purpose of this project is to help the retailer understand the properties of products and outlets that play crucial roles in predicting sales. The original data can be [found here](https://datahack.analyticsvidhya.com/contest/practice-problem-big-mart-sales-iii/#About) which contains 12 columns and 8523 rows. After spending much time researching, a fun fact was founded that the original data set was from India and the currency is in Rupees, and it help explains the price range in the dataset.

## Data Dictionary

![image](https://user-images.githubusercontent.com/126204698/229249068-9d421384-691b-4418-9268-4468b9de86ec.png)

## Key Questions

- What are the top selling items?

![image](https://user-images.githubusercontent.com/126204698/229251339-7f9acb61-57cf-43f3-afde-9bbb71f0218d.png)

- Does outlet type affect sales?

![image](https://user-images.githubusercontent.com/126204698/229251379-fde0b3ca-1bec-4ede-ae16-358b44a5260e.png)

From the visulization data above, different size of outlets does affect sales. Supermarket Type 1 has the most sales whilst Grocery stores with the least

- Does where the item locate affect sales?

![image](https://user-images.githubusercontent.com/126204698/229251403-c0a482be-3b0a-4aa9-9fac-86e9b3d447c3.png)

The results above suggest there is a negative correlation with -.13 r value between Item_Outlet_Sales and Item_Visibility. It can also be concluded that there is very limit relationship whilst comparing these two.

## Key Insights

### Coefficients

![image](https://github.com/hawkeyedatatsai/food-sales-predictions/assets/126204698/ad3b0c3d-d7d0-453f-9465-52451b4989a4)

Top 3 most impactful features include:

- Outlet_Type_Supermarket Type3:
For items being sold at Type 3 Supermarket, it changes model prediction to increase the item outlet sales by 1624.808 rupee.

- ITEM MRP:
For every 1 rupee ITEM MRP increased, it will increase the item outlet sales by 984.315 rupees annually.

- Outlet type grocery store:
When the item is switched to be sold at grocery store, the model predicts the annual sales to drop by over 1741 rupees.

### Feature Importances
![image](https://github.com/hawkeyedatatsai/food-sales-predictions/assets/126204698/a3d6e098-fe46-4621-9aec-914c36a82e7e)


The Top 3 most important features from the tuned decision tree are
- Outlet_Type_Grocery Store
- ITEM MRP
- ITEM Visibility
- Outlet_Type_Supermarket Type3
- ITEM Weight

## Global Explanations

### Summary Plot - Bar

![image](https://github.com/hawkeyedatatsai/food-sales-predictions/assets/126204698/d0eb0c70-b23c-4a8e-8ef5-e315e97617a4)

### Summary Plot - Dot

![image](https://github.com/hawkeyedatatsai/food-sales-predictions/assets/126204698/8a97d07c-b7a5-499a-9c46-b81057a8b73e)

## Local Explanations

### Item_MRP

#### Lime tabular explanation
![image](https://github.com/hawkeyedatatsai/food-sales-predictions/assets/126204698/52797a18-1ee2-42e0-99bb-9303d2864790)

#### Force Plot
![image](https://github.com/hawkeyedatatsai/food-sales-predictions/assets/126204698/4d9d4fd9-efa2-4ae0-acfb-d74143561e40)

### Item_Visibility

#### Lime tabular explanation
![image](https://github.com/hawkeyedatatsai/food-sales-predictions/assets/126204698/af75bcf3-69c1-4f91-8864-787d8a259fd1)

#### Force Plot
![image](https://github.com/hawkeyedatatsai/food-sales-predictions/assets/126204698/754819a7-cacb-4e3d-b300-b5f88bf6dabc)


## Machine Learning Models Comparison
- Linear Regression
- Decision Tree Regressor
- Bagged Tree Regressor

## Comparing MAE, MSE, RMSE and R2 for Each Regression
![image](https://user-images.githubusercontent.com/126204698/229249968-d5af2506-b237-464b-879c-7c8a5edf5936.png)

- All three models generate similiar R2 test score but Decision tree has the highest.

- All three models generate similiar RMSE test score but Decision tree has the lowest.

- From conclusions above, I would recommend to use decision tree model.

# Contact
Please direct all communications to Henry Tsai at hawkeyedatatsai@gmail.com

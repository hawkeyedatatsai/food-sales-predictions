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

Results above suggest there is negative correlation with -.13 r value between Item_Outlet_Sales and Item_Visibility. It can also be concluded that there is very limit relationship whilst comparing these two.

## Key Insights

### Feature Importances




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

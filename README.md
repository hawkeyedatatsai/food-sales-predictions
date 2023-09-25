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

## Machine Learning Models Comparison
- Linear Regression
- Decision Tree Regressor
- Bagged Tree Regressor

## Comparing MAE, MSE, RMSE and R2 for Each Regression
![image](https://user-images.githubusercontent.com/126204698/229249968-d5af2506-b237-464b-879c-7c8a5edf5936.png)

- All three models generate similiar R2 test score but Decision tree has the highest.

- All three models generate similiar RMSE test score but Decision tree has the lowest.

- From conclusions above, I would recommend to use decision tree model.

## Key Insights

### Coefficients From Linear Regression Model

![image](https://github.com/hawkeyedatatsai/food-sales-predictions/assets/126204698/ad3b0c3d-d7d0-453f-9465-52451b4989a4)

Top 3 most impactful features include:

- Outlet_Type_Supermarket Type3:
For items being sold at Type 3 Supermarket, it changes model prediction to increase the item outlet sales by 1624.808 rupee.

- ITEM MRP:
For every 1 rupee ITEM MRP increased, it will increase the item outlet sales by 984.315 rupees annually.

- Outlet type grocery store:
When the item is switched to be sold at grocery store, the model predicts the annual sales to drop by over 1741 rupees.

### Feature Importances From Tree Based Model
![image](https://github.com/hawkeyedatatsai/food-sales-predictions/assets/126204698/a3d6e098-fe46-4621-9aec-914c36a82e7e)


The Top 3 most important features from the tuned decision tree are the same to coefficients. The model suggests that these three features are the ones that were used extensively and repeatedly during the training process. However, feature importance does not indicate directionality.

## Global Explanations

### Summary Plot - Bar

![image](https://github.com/hawkeyedatatsai/food-sales-predictions/assets/126204698/d0eb0c70-b23c-4a8e-8ef5-e315e97617a4)

Summary plot and original feature importances suggest same top three features: ITEM MRP, Outlet_Type_Grocery Store and Outlet_Type_Supermarket Type3.

### Summary Plot - Dot

![image](https://github.com/hawkeyedatatsai/food-sales-predictions/assets/126204698/8a97d07c-b7a5-499a-9c46-b81057a8b73e)

#### interpret the top 3 most important features
- Item_MRP
From the red dots on the right, we can observe that the greater the maximum retail price of an item, the higher chance the model will predict a higher item outlet sales.

- Outlet_Type_Grocery Store
From the negative values (blue dots on the right). If items are less likely to be sold in Grocery Store, it predicts a higher value in sales.

- Outlet_Type Supermarket Type3
From the red dots on the right, if items are sold in Type3 Supermarket, the models predicts it has a higher value in sales.

## Local Explanations

### Item_MRP 
I select the sample with highest item mrp because it is the most obvious important feature through global explanation.

#### Lime tabular explanation
![image](https://github.com/hawkeyedatatsai/food-sales-predictions/assets/126204698/52797a18-1ee2-42e0-99bb-9303d2864790)

##### Interpretation of LIME table
The model predicts this sample has a sales value of 4055.65.

There are several features that were associated with price increased and the following two features have the most significant impact:

outlet type grocery store = 0, which means item not being sold at grocery actually helps increase sales price.

item mrp > .78, whereas this sample has an item mrp of 1.97.

The model predicts that outlet type supermarket = 0 decrease the pricing. In other words, the type of outlet plays an significant role with this sample.

#### Force Plot
![image](https://github.com/hawkeyedatatsai/food-sales-predictions/assets/126204698/4d9d4fd9-efa2-4ae0-acfb-d74143561e40)

##### Interpretation of Individual Force Plot
- Base value suggest 2210 dollars in sales

- Item_MRP, with the value of 1.968, is the most important feature for this item and it is pushing the prediction toward a higher value (red bar).

- Outlet_Type_Groery_Store = 0 (item not sold at Grocery Store) is also pushing the prediction toward a higher value.

- Outlet_Type_Supermarket Type3= 0 (item not sold at Supermarket Type3) pushing prediction toward a lower value.

### Item_Visibility
I select the sample with highest item visibility because of my personal interest on understanding the displaying and presentation area of items.

#### Lime tabular explanation
![image](https://github.com/hawkeyedatatsai/food-sales-predictions/assets/126204698/af75bcf3-69c1-4f91-8864-787d8a259fd1)

##### Interpretation of LIME table
- The model predicts this sample has a sales value of 315,15.

- There are two features that have the most significant impact overall and both have to do with price decrease, and one again, the model is telling us how important the selling place with the prediction.

- According to the model, item MRP and item type seafood = 0 make the biggest positive impact on this specific sales. The latter could have to do with the fact that seafood needs addition expenses for freezers and storage and concerns about shorter expiration date.

- After all, it should be the sales drives item visibility, not the other way around.

#### Force Plot
![image](https://github.com/hawkeyedatatsai/food-sales-predictions/assets/126204698/754819a7-cacb-4e3d-b300-b5f88bf6dabc)

##### Interpretation of Individual Force Plot
- base value suggest 2210 dollars in sales whilst predicted sale price is 315.15, much less than base value.

- Outlet_Type_Groery_Store = 1 (item sold at Grocery Store) AND Outlet_Type_Supermarket Type3= 0 (item not sold at Supermarket Type3) is pushing the prediction toward a lower value.

- Item_MRP, with the value of .2302, is the most significant feature pushing the prediction toward a higher value (red bar).

# Contact
Please direct all communications to Henry Tsai at hawkeyedatatsai@gmail.com

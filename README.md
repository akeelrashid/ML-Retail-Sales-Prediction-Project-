# ML-Retail-Sales-Prediction-Project--
# Problem Statement:
Rossmann operates over 3,000 drug stores in 7 European Countries.Currently,Rossmann store managers are tasked with predicting their daily sales for upto six weeks in advance.Store sales are influenced by many factors,including promotions,competition,school and state holidays,seasonality,and loclity.With thousands of individual managers predicting sales based on their unique circumstance the accuracy of result can be quite varied.You are provided with historical sales data for 1,115 Rossmann stores.The task is to forecast the 'Sales' column for the test set.Note that some stores in the dataset were temporarily closed for reburisment

# Project Summary:
I have been provided with historical sales data for 1,115 Rossmann stores.My task is to forecast the sales and it has been mentioned that some of the store were temporarily closed for rebursment during that period sales were 0. I have two datasets.firstly i imported both the datasets.One dataset is roaman store which contains 1017209 rows and 9 columns.The dataset doesn't contain any null or duplicated values.It gives us inforamation about the type of store,sales in each store by what date through how many number of customers.Also whether the sale was affected by closure of shop on weekends or or any kind of stateholiday or schoolholiday.It also gives on how sales was affected on applying promo.The other dataset is store which has 1115 Rows and 10 Column.This dataset contains too many null values in different columns.It provides information like type of store and what is assostment level used in store,how far away is competitor from store,since how long is competitor there in the market and how often is promo applied on the store.

I droped some colunms from store datset which contains too many null values and filled some fearture which contains very less amount of null values and then i merged both the datasets.I then checked for outliers and there were some columns which contained outliers and then treated them using percentile method.

Then i performed EDA (univeriate,Biveriate and Multiveriate analysis) to extract some useful insights from the data.Then i performed Feature Enginering and data preprocessing in which i performed label encoding for categirical features and defined some new features also ,i calculated VIF to find out Multicolinearity between the features and selected important feature for futher analysis.Then i splitted the data in dependent and independent variables and transformed the data using Standard Scaler.Then i split the data in x_train,y_train,x_test,y_test with test size as 0.2.

Then at the end i implemented Model on my data like Linear Regression,Ridge Regression,Lasso Regression,Decision Tree,Random Forest and XGBoost model on my data. Based on the performance of all the models, i have selected XGBoost model as the final prediction model. The XGBoost model outperformed the other models in several key aspects, making it the preferred choice for prediction

# Conclusion:
EDA helps us to extract some useful insights from the data.some of the insights drawn from the data are as:
* It has been find out that **Day-1** i,e Monday has got maximum Sales and **Day-7** i,e Sunday has got least
* when any kind of Promo was applied ,during that period sales got almost doubles
* After **october** there was a very large growth in sales that might be due to festival season.**December** shows maximum sales may be because of christmas and new year
* It was find out that **Store b** sales has been inceased from 2013 to 2015 and in 2013 **store d** has maximum sales and in remaining years store b has maximum sales
* Sales are highest for the **assortment b**.
* it was also observed that mostly the competitor stores weren't that far from each other and the stores densely located near each other saw more sales.
* **School Holiday** doesn't really affected sales but there little more sales during school Holiday Period
* Whether **state holiday** or not there was good amount of sales on both the occassions and it was find out that only **3%** of sales is effected by stateholiday.So overall sales doesn't depend on stateholiday
*The customers and sales are positively corelated to each other i,e more customer visits the store more will be sales
* It was observed that Running promo continously has not been that much effective towars increasing Sales
*  **Promo,Open and customer** has positive correlation with **Sales** means that if the shop is ruuning any promo more customers will visit the store there will be more sales
* **State holiday** has very low negative correlation with sales as sales is not affected by state holiday same case with the school holiday

* I have implemented Linear Regression,Ridge Regression,Lasso Regression,Decision Tree,Random Forest and XGBoost model on my data. Based on the performance of all the models, i have selected XGBoost model as the final prediction model. The XGBoost model outperformed the other models in several key aspects, making it the preferred choice for prediction.

The XGBoost model achieved high R2 score of 0.9819 on the test data and r2 score of o.99 in trainig dataset

also the XGBoost model achieved lower Mean Squared Error (MSE) and Root Mean Squared Error (RMSE) values compared to the other models. With an MSE of 185,145.49 and an RMSE of 430.29, the XGBoost model exhibits smaller prediction errors and improved accuracy in predicting the target variable.

As the XGBoost model displayed consistent performance across various evaluation metrics, including the R2 score, MSE, and RMSE. Its high performance on both the training and test data indicates good capabilities and reduces the risk of overfitting.

Additionally the residuals analysis revealed mean and median values of 0.45 and -2.73, respectively.The well-behaved residuals indicate that the XGBoost model effectively captures the underlying patterns in the data and minimizes systematic errors.

Considering the model's strong predictive performance, lower prediction errors, and consistency across evaluation metrics, the XGBoost model is the preferred choice as the final prediction model.

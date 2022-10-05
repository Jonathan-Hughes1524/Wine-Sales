# Wine-Sales
Analyzing data of Spanish Wines to predict sale price using Machine Learning

#Author: Jonathan Hughes

#Business problem:
Predicting the sales price of wine based on features that have a correlation to wine price to optimize sales.

#Data:
The data can be found in the link below:
https://drive.google.com/drive/u/0/folders/1IIsScg3Mtcjd_EaXGlMu-FvvkcC3Z1bs
This data provides us with information about the wine. For example the winery, wine type, boldness, rating, etc.

Methods:
  * The first methods that I used were data cleaning.
  * I checked the data for duplicates and deleted those.
  *Also checked for any missing data and made a decision on what to do with missing data. 
  * After that visualizations were made to represent the data.
  * Then used preprocessing to prepare the data to be used in Machine Learning.
  * After preprocessing ran the data through a Linear Regression and KNN. 
  * Evaluated the models with MAE, MSE, RMSE and R^2 metrics to determine best model.

# Correlation visualization
![image](https://user-images.githubusercontent.com/108833661/193129047-edc4a7be-f1b4-41a0-9857-8168ddb78dcb.png)

This graph shows us the correlation between the price and other features. It shows us whether the feature will have a positive, negative or no correlation to the price. This is helpful when determining what featurest to focus on when making a wine. 

#Visualization of rating and price
![image](https://user-images.githubusercontent.com/108833661/193129120-12b121f9-20b1-4a56-bba3-44d0204a4ba6.png)

The graph above shows how the rating affects the price of thwe wine. As seen in the graph the higher priced wines have the better ratings. It is important to get a good rating on the wine if you wish to charge more for the wine. 

Based on the association some columns were dropped befroe machine learning. The region and country were dropped from the model. 

# Model
Multiple models were ran including a KNN model, a hypertuned KNN model, Linear Regression, and a PCA fit on both KNN and Linear regression. The model that performed the best was the PCA KNN model. Below is a copy of the predictive scores of the test model. 

Test Evaluation
MAE 56.91590310444923,
 MSE 31656.65545402059,
 RMSE: 177.92317289780044,
 R^2: 0.533457253302263 

# Recommendations:
My recommendation is to use the PCA KNN  model to predict the sales price of the wine. This will allow us predict the sale price of wine within $57 of the actual price either above or below. This gives us a good range to work with in pricing each of the wines.  

# Limitations and next steps:
I would like to consult a wine expert on helping determine if more features need to be dropped to improve scores

# For further information:

For any additional questions please contact

jhughes1524@gmail.com

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

#Correlation visualization
![image](https://user-images.githubusercontent.com/108833661/193129047-edc4a7be-f1b4-41a0-9857-8168ddb78dcb.png)
This graph shows us the correlation between the price and other features. It shows us whether the feature will have a positive, negative or no correlation to the price. This is helpful when determining what featurest to focus on when making a wine. 

#Visualization of rating and price
![image](https://user-images.githubusercontent.com/108833661/193129120-12b121f9-20b1-4a56-bba3-44d0204a4ba6.png)
The graph above shows how the rating affects the price of thwe wine. As seen in the graph the higher priced wines have the better ratings. It is important to get a good rating on the wine if you wish to charge more for the wine. 

#Based on the association some columns were dropped befroe machine learning. The region and country were dropped from the model. 

#First model is KNN
After preparing the data for machine learning a KNN model was attempted on the data. The model was ran and evaluated using  mean squard error and r2 scores.  Which are shown below. 
KNN Training RMSE: 116.43955051980967
KNN Test RMSE: 171.91515129997822
-----
KNN Training R2: 0.8217290686713979
KNN Testing R2: 0.5644332494491799

Then the model was hypertuned to try and increase the performance. The model was ran through a grid search to find parameters to help the model perform. The new model was called KNN_GS and evaluated on the same metrics.
KNN_GS Training RMSE: 136.37236655701446
KNN_GS Test RMSE: 174.7422276892105
-----
KNN_GS Training R2: 0.7554699441517364
KNN_GS Testing R2: 0.5499900168605133

#Second Model is a Linear Regression
A linear regression model was ran to see how well it would perform on the data. It was evaluated with the same metrics as the KNN models. The results are shown below.
RF Training RMSE: 90.22762712274984
RF Testing RMSE: 75352984217647.19
RF Training R2: 0.8929569278446096
RF Testing R2: -8.36810893752042e+22
As seen these scores need some improving on the model if it is going to be used. 

 #The third model is a linear with PCA applied
First I ran the Linear model with PCA applied to it. This was done to see if we could improve the model and get better evaluation metric scores. The scores are shown below. 
PCA Linear Training RMSE: 114.82922005839413
PCA Linear Test RMSE: 179.98282721316815
-----
PCA Linear Training R2: 0.8266258588186874
PCA Linear Testing R2: 0.5225932540329836

#The fourth model is a KNN with PCA applied. 
Then I ran the Linear model with PCA applied to it. This was done to see if we could improve the model and get better evaluation metric scores. The scores are shown below. 
PCA KNN Training RMSE: 113.81554626080565
PCA KNN Test RMSE: 177.92317289780044
-----
PCA KNN Training R2: 0.8296733255846894
PCA KNN Testing R2: 0.533457253302263



#Recommendations: My recommendation is to use the KNN  model to predict the sales price of the wine. This will allow us to select the best price of a wine to optimize the sales of each wine. This will allow us to not overcharge the customer and prevent sales, while also allowing us to make the hightest profit off the wine sales.

#Limitations and next steps: I would like to consult a wine expert on helping determine if more features need to be dropped to improve scores

For further information: For any additional questions please contact
jhughes1524@gmail.com

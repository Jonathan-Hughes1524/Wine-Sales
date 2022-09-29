# Wine-Sales
Analyzing data of Spanish Wines to predict sale price using Machine Learning

Author: Jonathan Hughes

Business problem:
Predicting the sales price of wine based on features that have a correlation to wine price to optimize sales.

Data:
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

Correlation visualization
![image](https://user-images.githubusercontent.com/108833661/193129047-edc4a7be-f1b4-41a0-9857-8168ddb78dcb.png)

Visualization of rating and price
![image](https://user-images.githubusercontent.com/108833661/193129120-12b121f9-20b1-4a56-bba3-44d0204a4ba6.png)

Based on the correlaton we can see what makes an impact on price. Unneccessary columns were dropped and then ran throught machine learing.

First model is KNN
After running the information through a KNN model it was then hypertuned to get the best result. The predictions are listed below.
KNN_GS Training R2: 0.6920514701113538
KNN_GS Testing R2: 0.7249289075982572

Second Model is a Linear Regression
After running the data through a Linear Regression model it was then ran through PCA to further tune it. The final predictions are listed below. 
Training Accuracy 0.3038688490958783
Testing 0.30742172055348516
As we can see these numbers are not high enough for us to make a confident precition in sales price.

The third model is a KNN with PCA applied. The predictions are listed below.
Training Accuracy 0.5894491170627614
Testing 0.4022213211130363
The predictions here did not increase on our original KNN but rather went down. This shows us that the orignal KNN is the better model.

Recommendations: My recommendation is to use the KNN hypertuned model to predict the sales price of the wine. This will allow us to select the best price of a wine to optimize the sales of each wine. This will allow us to not overcharge the customer and prevent sales, while also allowing us to make the hightest profit off the wine sales.

For further information: For any additional questions please contact
jhughes1524@gmail.com

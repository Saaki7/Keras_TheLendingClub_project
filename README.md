# Keras_TheLendingClub_project
LendingClub is a US peer-to-peer lending company, headquartered in San Francisco, California. LendingClub is the world's largest peer-to-peer lending platform. 
Our Goal was from the given historical data on loans with information on whether or not the borrower repaid the loan, a model was built to predict wether or nor a borrower will pay back the loan.
# Index
 1. Data Overview and loading
 2. Exploratory data analysis
 3. Data PreProcessing
 4. Dealing Categorical features
 5. Normalizing
 6. Model building and evaluation.


**1. Data Overview and Loading**

Imported several libraries that are useful for the implementation of the project. Pandas, Numpy, Matplotlib, Seaborn are some among them for several data analysis and visualization purposes. Loaded the data that I got from Kaggle resources and had a brief study of the Data frame.


**2. Exploratory Data Analysis**

Developed several plots by setting hue as _"Loan_status"_ i.e visualised behaviour of all the features for the people who has paid the loan and people who hasn't. Constructed heat
maps between the features describing the correlation between them.

Here is a heat map showing the correlations between the features
![Keras_heatmap](https://user-images.githubusercontent.com/86612650/130443072-de46afac-ed63-49de-af89-07f68a4c8dfd.png)

Here is a bar chart that provides information about the borrowers grade and their count with hue as _Loan Status_
![grade](https://user-images.githubusercontent.com/86612650/130443711-9158a435-a993-49fd-9723-a84e74f5c291.png)


**3. Data PreProcessing**

Dealt with the _NullValues_ of each column seperately depending on the type and importance of the columns. Some features need null values to be replaced with the means where as some others needed to be dropped as they are unimportant in the model building.
_Mort_accs_ feature has more null values and also it is very important feature so nulls cant be deleted. I found the feature which has more corelation with this feature and by applying some aggregations I fiiled these null values in _Mort_accs_ feature.


**4. Dealing Categorical features**

Using dummy variables from Pandas, changed some categorical features to 1 or 0 features.


**5. Normalising**

After spliting the data using as *train_test_split* used a MinMaxScaler to normalize the feature data X_train and X_test. As I don't want data leakge from the test set, so I only fit on the X_train data.


**6. Model Building and Evaluation**

Built a decent model using _Sequential_ model from Keras.models with addition of _Dense_ and _Dropout_ layers. The activation function used is __RELU__. Relu is used over sigmoid because it is faster as gradient descent works better on it. The cost function used is "Binary_cross_entropy" and the optimiser being "ADAM".




 

# Home-Credit-Default-Risk
My take on the Home Credit Default Risk Competition on Kaggle. The objective of the competition is to predict the probability of a loan default.

## Dataset
The [dataset](https://www.kaggle.com/competitions/home-credit-default-risk/data) for the competition is provided on Kaggle by Home Credit, a non-bank financial services company.  
For this particular project, I have used only the loan application data (application_train.csv and application_test.csv).
![image](https://github.com/gautam-girotra/Home-Credit-Default-Risk/assets/69039186/7f2c8ab7-8c6a-435b-9d31-020a197a2586)  

## Approach
### EDA : 
For the exploratory data analysis, I have used the matplotlib and seaborn libraries.
For categorical/discrete numerical features I used pie charts and bar charts.
For continuous numerical features, I used cumulative distribution functions, distribution plots, and box plots. 
To find outliers, Interquartile range has been used.  

### Preprocessing :
Using the insights from EDA, domain knowledge, and some trial and error, various features have been engineered in order to improve the dataset.
For imputing missing data, I have used mean, median, and mode.  
According to the number of unique values present in the respective categorical columns, I have encoded them using Label encoding/One Hot Encoding. 
I have used Sklearn's Standard Scaler to standardize the dataset.

### Modelling :
I compared the performance of different classification algorithms like Logistic Regression, Random Fores, Gradient Boosting, LightGBM, etc.
Out of these LightGBM and Gradient Boosting performed the best.

### Hyperparameter Tuning :
I have used the Optuna library to optimize the hyperparameters for the LightGBM classifier.

### Results :
Using just one of the 7 data files, I was able to achieve an roc_auc score of **0.753** on the test dataset.
![image](https://github.com/gautam-girotra/Home-Credit-Default-Risk/assets/69039186/88c12038-336e-4008-84d0-ef086b6cd8ff)

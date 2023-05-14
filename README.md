# Regression_project
Creating a Regressive predictive model for Counterfeit Medicines Sales data with machine learning algorithms using Python.

Counterfeit medicines are fake medicines which are either contaminated or contain wrong or no active ingredient. They could have the right active ingredient but at the wrong dose. Counterfeit drugs are illegal and are harmful to health.

I got Counterfeit Medicines Sales data,training and testing data both, which contains several features. As it was not fit for directly creating predictive model from the given data,i have to make it to go through data preprocessing process.
1.Combined the testing and training data 
2.Listed out the features name,their datatypes, number of unique values and number of null values in each of the columns.
3.Dropped the column Active_since and added a column year in its place containing number of years from current date to the given year in the column.
4.Dropped Medicine_ID column.
5.As Counterfeit_weight column contains some null values,so replaced null values with mean of the training data.
6.Created dummy variables for the columns DistArea_ID, Medicine_Type, SidEffect_Level, Area_Type, Area_City_Type, Area_dist_level
7.Divided the training and testing data.

Now, used training data for creating predictive models.
1. LinearRegression
2. Lasso
3. Ridge
4. DecisionTreeRegressor
5. RandomForestRegressor
6. GradientBoostingRegressor
7. XGBRegressor
8. MLPRegressor(Neural network)
9. KNeighborsRegressor
10. SVR(Support Vector Regressor)
11. Stacking of 7 different models
After fitting data into these above models,got some Mean absolute error for each of these models.
[['LinearRegression', 830.0501468413154],
 ['Lasso', 824.6251915497413],
 ['Ridge', 826.5080690425511],
 ['DecisionTreeRegressor', 768.2534880814219],
 ['RandomForestRegressor', 763.9811503098795],
 ['GradientBoostingRegressor', 773.993921730715],
 ['XGBRegressor', 795.2578689864172],
 ['NN_MLPRegressor', 773.824813373666],
 ['KNeighborsRegressor', 870.382600209468],
 ['SVR', 1295.6668221980908],
 ['stacking', 940.6105852126099]]
 
 As the RandomForestRegressor gives the least error,created a model for it.

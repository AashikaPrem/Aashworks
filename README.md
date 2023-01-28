# Exploratory Data Analysis

The OCG, a consultant group located in Windsor, Ontario that serves clients from various sectors including IT and non-IT, conducted a survey of 200 clients to measure satisfaction with their services. Data were processed, including data quality assessment, transformation, and reduction, before analysis. Explanatory data analysis was used to understand distribution and patterns, and predictive analysis, including linear regression, logistic regression, and K nearest neighbor, was used to predict and classify results. Dependent variables were recommendation and partnership, while independent variables included customer type, industry type, firm size, region, client portfolio management, innovative project management, responsiveness, expertise, competitive consulting fee, communication, and implementation. Results showed satisfaction has a positive relationship with recommendation and potential for future partnership.




## Documentation

**Data Pre-Processing**

Data pre-processing is the idea of transforming the raw data into a clean data set. Pre-processing data makes it simpler to analyze and use. The accuracy of our model is improved by removing data discrepancies or duplicates. The actions we took to prepare the dataset are listed below.

**Data Quality assessment**

The accuracy of the data was verified by assessing its truthfulness, completeness, and reliability. Linear regression was performed, and recommendations were compared across variables by splitting three qualitative customer types into two. Performing data quality assessment helps in effectively analyzing and computing the correlation matrix.

**Data Transformation**

To perform logistic regression and to compare the variation of partnership across the various variables like customer type, industry type, firm size, region, etc. we substituted the binary variables 0s and 1s with valid numerical labels for the current trend to be captured.

**Data Reduction**

There was no room for data reduction in our study because we used every piece of information available in the survey data. In this way, we made sure that the data quality was boosted and that no values were inaccurate or missing, which will lead to high-quality mining results.

**Data Analysis**

Our data analysis is divided into two categories: exploratory and predictive. Through exploratory analysis, we examine the distribution of data and uncover patterns by creating visualizations. This also helps us understand the relationship between variables in the dataset. The predictive analysis involves creating models to predict or classify results. The insights and recommendations for the business or stakeholders will be derived from the results of these analyses.

**Exploratory Data Analysis**

We performed exploratory data analysis for linear and logistic regression to predict the likelihood of recommendation and determine potential future partnerships as dependent variables. To do this, we needed to understand the effect of independent variables on them. The data included 5 qualitative variables (customer type, industry type, firm size, region, and partnership) and 9 quantitative variables (client portfolio management, innovative project management, responsiveness, expertise, competitive consulting fee, communication, implementation, overall client satisfaction, and likelihood of recommending OCG to others).



**Exploratory Data Analysis: Linear Regression**

We will analyze the impact of ratings on various factors by plotting the average ratings for different categories (such as customer type, industry type, firm size, and region) against quantitative data. This will allow us to identify patterns and relationships and understand how they affect the dependent variable. This is based on the survey we conducted, and the input ratings collected.

![image](https://user-images.githubusercontent.com/85166438/215278000-f6742961-9eaa-4708-b6a0-54563555f248.png)

![image](https://user-images.githubusercontent.com/85166438/215278017-21a01333-cff3-4c4d-a513-4da2170aa73e.png)

**Exploratory Data Analysis: Logistic Regression:**

To understand the potential of future partnerships across various factors we have plotted charts to capture the variation.

**Logistic Regression**

Logistic regression is a method used to predict the likelihood of a certain event occurring based on a set of independent variables. The outcome of the dependent variable is limited to either 0 or 1, as it represents a probability. This method involves applying a logit transformation to the odds, which is the ratio of the probability of success to the probability of failure. This can be represented mathematically as ln(pi/(1-pi)) = b0 + b1x1 + … + bkxk, where logit(pi) is the dependent variable, x is the independent variable, and beta (b) is the estimated coefficient, typically found through maximum likelihood estimation.
![image](https://user-images.githubusercontent.com/85166438/215278392-6c15f74f-d361-4c6f-8bca-8ae53fb005f6.png)
![image](https://user-images.githubusercontent.com/85166438/215278400-673b8090-e600-4d6f-8912-1c59959dc1fd.png)

**Below is the ROC curve obtained:**

![image](https://user-images.githubusercontent.com/85166438/215278416-b9019984-7eb2-44c7-8e4a-31ab2b907a0d.png)

**Predictive Analysis:**

After analyzing survey data through exploratory data analysis, we have found that the variable of "Recommendation" can be predicted using other independent variables. To accomplish this, we will be using Linear Regression, which is suitable for predicting quantitative variables like "Recommendation". Additionally, we will use Logistic Regression to classify potential future partnerships, as it is useful for determining the classification of "Partnership" in our case.

**Linear Regression**

Linear Regression is a technique for predicting the value of a dependent variable based on one or more independent variables. It estimates the coefficients of a linear equation that can be used to make predictions about the dependent variable. The equation can be represented as:
y = b0 + b1x1 + b2x2
Where "y" is the dependent variable, "b0" is the intercept, and "b1" and "b2" are coefficients for the independent variables "x1" and "x2" respectively.

**Bivariate Analysis**

To understand the relationship between the dependent and the quantitative variables we have utilized the bivariate analysis by creating scatter plots. This analysis will explain the variation of the independent variables and help us understand the correlation.
Below is the bivariate analysis:
Scatter plots for all the quantitative variables are created to understand the relationship with the dependent variable.
![image](https://user-images.githubusercontent.com/85166438/215278449-bf18f68e-d26c-4313-981f-a3ef6fe0302e.png)
![image](https://user-images.githubusercontent.com/85166438/215278453-8b12f6cc-9afb-4bc4-a615-5fd6315a12d0.png)

These Metrics show us the correlation between the quantitative variables and by understanding this we can remove collinearity and multi-collinearity from our Models.	

![image](https://user-images.githubusercontent.com/85166438/215278460-e7027b6a-4778-4d83-bd6c-b3447cd89514.png)

**K Nearest Neighbour**

KNN is a method that uses the proximity of data points to make predictions or classifications. It assigns a label to a data point based on the majority vote of surrounding points. It was created using variables that impact the potential future of a partnership and had a performance measurement of Specificity, Sensitivity, Precision, and F1 score of 0.947, 1, 0.934, and 0.966 respectively, which is better than logistic regression. It has no false negatives and accurate results for true positives, making it a better classifier.

**Classification Tree**

The classification tree, also known as the decision tree algorithm, is used to solve problems related to regression and classification. Its goal is to create a training model that can predict the class of the dependent variable by learning simple decision rules inferred from the training data. In this case, a classification tree was created using the Analytic Solver in Excel, and it was found that Specificity, Sensitivity, Precision, and F1 scores were all 1, indicating that the model is ideal. However, because the classification tree model has fewer data points, it is not reliable for predicting the dependent variable in this case.

**Conclusion**

**Insights and Recommendation**

•	Linear regression shows that firm size and satisfaction are key factors in a firm's decision to provide a recommendation to OCG.
•	Logistic regression shows that customer type 1, portfolio management, responsiveness, and satisfaction ratings are significant drivers of whether a firm will form a potential future partnership with OCG.
•	Firms that have been customers for less than 1 year are less likely to form a partnership, while firms that have been customers for more than 5 years are more likely to provide a recommendation and form a partnership.
•	The analysis also shows that there is a higher probability that firms in Ontario will not form a partnership with OCG.
•	If OCG receives better ratings for portfolio management and satisfaction, it will be more likely to form partnerships with other firms in the future.
•	KNN classification model that uses responsiveness and satisfaction as variables provides better results than logistic regression, as there are no false negatives in the confusion matrix and it provides more accurate results for true positives.

In conclusion, overall satisfaction ratings appear to be the most significant variable that can be used to predict the likelihood of recommendation and classification of forming potential future partnerships for OCG, hence OCG should focus on satisfying client needs in order to enhance its consulting practice.

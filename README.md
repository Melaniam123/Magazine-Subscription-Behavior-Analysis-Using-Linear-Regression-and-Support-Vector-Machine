# Magazine-Subscription-Behavior-Analysis-Using-Linear-Regression-and-Support-Vector-Machine
Leveraged the capabilities of logistic regression and Support vector machine classification, which can be used to accurately predict user purchase behaviour

# Introduction
This study focuses on helping a magazine company understand the decline in subscriptions over
the past year. Despite the increased amount of time people spent at home, the company observed
a decrease in readership. The objective is to analyze marketing subscriptions and gain insights
into the factors affecting subscription behavior. We will leverage the capabilities of logistic
regression and Support vector machine classification, which can be used to accurately predict
user purchase behaviour. Both methodologies are exclusive since logistic regression is based on
geometrical properties while SVM is based on statiscal properties. 
In this study, we aim to assist
a magazine publisher in determining the reasons for drop in the the subscription last year since
they anticipated that a person spending more time at home would increase reading and thereby
subscription.

# Methodology
In this study, we will assess two method: Logistic regression and Support vector
machines to understand user bhaviour and the accuracy of the model will be the key metric to
evaluate the reliability and effectiveness of the model. Evaluating predictvie metrics like
Accuracy Rate, Precision, Recall will enable the policymakers generate insights into which
factors have a significant influence over user behaviour and improving readershop and are
contributing to improved subscription.

# Exploratory Data Analysis 

Income variables to have outliers present in the data.
Therefore, we treated the outliers to range within the IQR (inter quartile range) as adjusted. Assessed the dataset of non unfirm values or characters like ‘?’ or NAN. Due to multiple factors and repetitive variables we paired different sub categories such as in Ecuation,
we paired 2n Cycle into “Masters”. We then replaced Together with “Common-Law” and paired
YOLO, Alone and Absurb as “Single”. We calculate Age from Birth year by subtracting it from
current year. We summed up all Accepted_CMP into Accepted Offers, which were users who has
accepted to subscribing for magazine. Similarly, we summed kid home and teen home into Teens
and all the purchased items into Total spends.

# Some quick notes
1) Maximum of our users to be married. and
common-law/ live-in users to be second highest.
2) Graduates could possibly be our target
audience who would be interested in our magazine subscription
3) There are constant purchase in <20 to 100 days
which assesses the purchasing behaviour of the individuals.
4) The income distribution  of individuals are within the range of
40,000-60,000
5) The spending patterns across different product types, where
most users are spending on Wine consumption and Meat products and least on Fruits. This could
also be interpreted in a way that cost of meat and wine is far more superior than fruits.
6) Highest purchase were visibly recorded from stores and web purchases while the lowest were recorded, from deals.
7) The income distribution by Marital Status and
Education where Married, Divorced and Widow have a higher Income while Singles have a
lower income range, similarly PhDs and Graduates have a higher income range than the others indicating purchasing power
8) Widow and Single’s have a higher response rate compared
to Married , Common Law who often tend to ignore these deals.

So lets get started on data modelling

We conducted Variance Inflation Factor analysis to assess the degree of multicollinearity
in our study of regression. Multicollinearity occurs when there is a correlation between numerous
independent variables. The findings of the analysis included that all variables had an VIF of <5.
A VIF of >5 depict that the variables have higher multicolinearity and hence must be eliminated
from the analysis.

Logistics Regression Results Summary
From the results below we can interpret the following:
Model Information:
● Dependent Variable: Response
● Number of Observations: 1568
● Model: Logit (logistic regression)
● Method: Maximum Likelihood Estimation (MLE)
Model Fit:
The Pseudo R-squared: 0.3633, Log-Likelihood: -421.79, Log-Likelihood Ratio (LLR)
p-value: 3.246e-82, Converged: False, LL-Null: -662.46. The model consists of approximately
36.33% of the variation from the response variable. Note, that the Pseudo R-squared values must
be interpreted with caution and must not be directly compared to R-squared values from a inear
regression.

![image](https://github.com/Melaniam123/Magazine-Subscription-Behavior-Analysis-Using-Linear-Regression-and-Support-Vector-Machine/assets/97692152/0ded2d6c-e0c5-4c85-8699-d238715c0efe)

A loglikelihood isa measure of how well a logistic regression fits the observed data where higher
the loglikelihood the better, however in this case it is -421.79 which is essential to compare with
the results of an alternet model. The LLR P-values is a measure to determine the statistical
significance of the model as a whole. While in this case, the LLR p-value is very small
3.246e-82, indicating strong evidence to reject the null hypothesis and be certain that the model
significantly improves the fit.

The convergence values is False, which indicates that the p-value and coefficients estimated by
the model may not be reliable and we must look at the other predictive indicators and exercise
caution while interpreting results for opportunities.

Overall Accuracy
= 0.8898809523809523, Precision = 0.7049180327868853, and Recall = 0.434343434343436.
Overall accuracy represents the proportion of correctly classified observations from the total
number of instances in the data and in this case, the model achieved an overall accuracy of
approximately 0.8899, which depicts that the model correctly predicted the outcome for the
given percentage. Similarly, the precision suggests that approximately 0.7049 of the instances
predicted as positive by the model were true positives, since precision is an indication of the
number of positive predictions made by the model are actually correct, predicting a positive
subscription behaviour. Recall of 0.4343, indicates that the model correctly identified around
43.43% of the actual positive instances whoa actually subscribed to the magazine.

As we evaluate the confusion matrix, it can be assessed that the predictions were obtained
by comparing the predicted probabilities with a threshold of 0.5 which provides a binary
classification result (0 or 1) for each instance in the train set and test set.

Support Vector Machine Results Model
The SVM model, built with a linear kernel, is taking into account all the features of the
data frame. We imposed a 70:30 train-to-test split ratio as a result of the training data set of 70%
and testing data set conatins 30% of the split.

The second SVM Model was created only using the significant variables using the SVM
Classification Model are ‘MntMeatProducts', 'MntGoldProds', 'NumDealsPurchases',
'NumStorePurchases', 'NumWebVisitsMonth'.

# Results 
Models Accuracy Precision Recall
Linear regression Accuracy 0.8898809523809523 Precision 0.7049180327868853 Recall 0.43434343434343436
STUDY OF LINEAR REGRESSION AND SVM
SVM Model 1 (All data) Accuracy 0.8645833333333334 precision 0.6333333333333333 Recall 0.1919191919191919
SVM Model II ( Significant Variables) Accuracy 0.8541666666666666 Precision 0.5555555555555556 Recall 0.050505050505050504

# Conclusion

We can conclude, by assessing the model results and confirming that the logistic
regression model is a better suited model to study the user subscription behaviour since the
accuracy, precision and recall score is higher and reliable. Along with the accuracy the number
of true positives and the correctful categorization of true positives is higher than the SVM model

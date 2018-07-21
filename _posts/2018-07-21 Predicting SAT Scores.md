---
layout: post
title: Predicting SAT scores of Chicago
---

# Exploring Factors Contributing To SAT Scores in Chicago

## The Challenge

SAT scores in vary from student to student. There are reasons to explain for the reasons for their results. However, I want to look at the reasons within a statistical frame of mind.

## Finding the Data

I am aware that finding data for individual SAT performance and related demographics would be nearly impossible. Therefore, I needed for a common ground factor. If the last sentence is confusing, let me explain. Looking at the City of Chicago data sets, I found many data sets with different rows, as such I can't perform regression. As such, I grouped my data by zipcode- the common ground factor and therefore resolving the issue of dimentionality.

From all the data sets, I pulled out the following variables:

- Median Income Household
- Number of Police Station
- Number of Restaurants with Permits to Eat Outside
- Number of “Street Lights Out” Reports
- Number of Abandoned Buildings Reported
- Selective Enrollment

Additionally, I used the following data from Atlas:

- Percent White
- Percent Black
- Percent Mexican


## The Procedure

# Split And Train And Multiculinearity

First, I checked for multiculinearity before proceding with tuning and building models. From the figure, I found %Black to be highly correlated with %White. Therefore, I removed %White as a explanatory variables.

# Checking Conditions:
 
I plotted my residuals against predicted to see if there is a pattern. I noticed a U shape from this distribution. I had to options, the first was to transform observations but I believe that I would lose interpreability of the model, so I chose to transform my attributes (x's). In such, I noticed _, _, _, needed to be changed. I need to make a note that even with changing my ACT into log did not change the shape of it to have homoskedacity and not outliers.

From each variable I found that reduced the non linear shape, I appended that modified variable into the model. I chose to do this because I know that Lasso and Ridge would decide which variables are important.

Third, I performed linear regression on the model with the transformed variable, checking the p-values through a t-test. From the data, I found some level of indication of the significance level for each explanatory variable. Ones that stood out at this moment is Median Income Household, Attendance of Selective Enrollement, and Number of Times Streetlights Go Out.

# Standardize and Lasso and Ridge
Followed then by standardizing my model. Soon, proceded with Lasso and Ridge in reduction of variables that do no contribute in a fashion that is statistically significan. I decided that I would fold 5 times with this model.

From Ridge, 

From Lasso, 





Notices: I should split and train my data even before performing multiculinearity 

Questions from this experiment:

What does standardizing do that just going straight to Lasso and Ridge wouldn't be ble to do


Split and Train my model first then check for multiculinearity but I am confused on the potential code that results from Split and Train. What is the process look like? What is the output? Do I get sections of the split variable? Do I get the test and if I do get the test, is test a portion of the whole data set?

Assuming that I do get an output from Split and Train my model that maybe be a new and great data set (splittraindata), I would then do the lr=LinearRegression() and do like lr.splittraindata or what? This would be to see the summary() or t-test.

Assuming that I splittraindata that is a new set of data, I check the conditions of linearity -- residual versus predicted, x vs residual, qqplot, wilkens-shapiro test. If x vs residual fails, transform the data. Following that, if y vs residual fails, then I can transform the y. However, we know that predicted comes as a product of x-values. Therefore, I would move forward with x maniupulation if the transformation of y loses meaning.

In which ever direction you go for translation, you have a new model with all these new variables. One question in here is if I should drop the predictor variable in question. Example: if X1 needs to be described as X^2, do I drop X1 and leave X^2. My time at linear regression at NU indicated that I should leave both in the model because forward step and backwards step and f-b step would take care of the elimination processs. In this case, Lasso and Ridge would do this elimination processs!

The question that I have about Lasso and Ridge is that yeah, I can get coef and intercept from best_Lasso and best_ridge, but I want to do t-test from this new data. IS that possible?

Overall, what is the process? How is the starting data being filtered and sorted through out this process? What is eligible for usage?






















# Linear Regression : Ecommerce Clothing Website

## Objective of the project
Business Problem : E-commerce company is trying to decide whether to focus their efforts on their mobile app experience or their website. We are here to help them make a data-driven decision.

## Data used in this project 
I've used the dataset [available on Kaggle](https://www.kaggle.com/iyadavvaibhav/ecommerce-customer-device-usage). The data includes information about customers of an e-commerce website, including the following:
- Avg. Session Length: Average session of in-store style advice sessions.
- Time on App: Average time spent on App in minutes
- Time on Website: Average time spent on Website in minutes
- Length of Membership: How many years the customer has been a member.

## Steps involved in the Analysis

- Exploratory data Analysis: 
  We've to answer the following question :
    - How are the client's time spent on each platform related to the amount that they spend per year?
           When visualizing using the jointplot on parameter 'Time on App', there doesn't seem to be much correlation between the time on the desktop website with the amount that clients spend per year. On the other side, jointplot on parameter 'Time on website' shows that there seems to be a small correlation between the time spent on the app and the yearly spending. This is probably because these clients tend to spend less time browsing on the phone. Maybe the payment process is faster on the app or the calls-to-action are more successful there.
          After analysing the pairplot, we see that there does seem to be one big positive correlation between two variables: the length of membership and the yearly expenditure. In the end we've created the lmplot to visualise the regression line.

- Splitting the Data : 
      After visualizing the parameters, We've to split the data into traing and test data. X are the predictors, and y is the target or output. What we want to do is create a model that will take in the values in the X variable and predict y with a linear regression algorithm. We use SciKit Learn library to create the model.

- Training the Model with multivariable regression using Scikit Learn : 
     we create the model and feed the training data to it. This model will tell us which input has the biggest impact in the output (yearly expenditure). As the plots suggested, we find that the most important coefficient is that of the "Length of Membership" predictor, followed by the 'Time on App' and the 'Avg. Session Length'. The time on website does not seem to be an important factor to the amount a customer spends per year.

- Predicting Test Data : 
    Once the model is trained, we should be able to use it to make our predictions and evaluate our model. The scatter plot used, plots the actual y values to the model's predictions. The model seems to behave accurately.

- Residuals : 
   Distribution plot is used to evalaute whether the residuals of the model's predictions are normally distributed.

## Conclusion:

  Interpreting this analysis requires careful consideration. According to our model, the length of membership is the most significant factor influencing customer spending—not the time spent on the app or website. Among the two digital platforms, mobile app usage has the strongest impact, while desktop website usage shows almost no correlation with spending.

This insight can be viewed in two ways:
- The desktop website may need improvements to drive more conversions.
- Customers are generally more influenced by mobile apps than desktop websites, suggesting a shift in focus toward enhancing the mobile experience.
  
Ultimately, the strategic direction should be guided by expertise in online marketing. However, our analysis provides valuable insights into predictor importance, helping businesses optimize their digital strategy effectively.

# Author
Vishnu Priya Sakthidharan.

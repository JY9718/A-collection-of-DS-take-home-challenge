# Exercises taken from 'A Collection of Data Science Take Home Challenge'


Ex1: Conversion rate EDA and AB-testing

The exercise is consist of 2 parts:

1. Perform exploratory data analysis to understand the conversion rate of an online shopping website
  
   Use model to predict the convereision rate
   
   Give recommendation to the marketing team in terms of how to improve conversion rate
   
2. Evaluate the AB testing result

   Understand whether the localized translation website (B test) is worse
   
   
Ex2: Employee retention analysis

This exercise has 3 challenges:

1. create a new dataframe to report employee headcount of each company at each date

  In order to obtain headcount at a date, I calculated net headcount = joiner at that date - quitter at that date (first groupby count() and then merge on date and 
  
  company), then calculated cumulative sum by using cumsum()

2. analyze the main factors driving the employment churn

I have engineered a new feature called early quitter rate to measure the percentage of employees who quit before a certain duration threshold (375 days)

Then it turned into a classification problem as we aimed to classify employees into early quitter and not early quitter.

I applied xgboost for this classification problem and plot feature importance.

The most important feature is salary, which makes sense as we could see from charts that higher salary shows lower early quitter rate. 

In addition, we could also see heatmap that other features such as seniority and dept are positively correlated with salary

3. discuss other possible data to be included

Since salary is the most important features, we could also collect offer salary in the next job for quitters, or salary increase speed, i.e. promotion or pay rise during employment tenure

other new features to be considered are work life balance or company/team culture

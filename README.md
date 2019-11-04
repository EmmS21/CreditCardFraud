# CreditCardFraud
Detecting fraudulent credit cards

This project uses data from Kaggle: https://www.kaggle.com/mlg-ulb/creditcardfraud to produce;
i.) a visualization of spending patterns (specifically seconds elapsed since the first transaction together with the size of said transactions) to understand possible spending patterns
ii.) transactions by the hour
iii.) a credit card fraud detection algorithm

I started off by using logistic regression as sort of a baseline for my classifiers.
I proceeded to use recursive feature elimination  to remove features of lower importance which would help reduce the complexiy of my model, decrease overall training time and hopefully lead to better predictions
After using this, I reran my logistic regression to assess whether there was a notable improvement in accuracy.

I proceeded to use xgboostclassifer together with the randomizedsearchCV module from sklearn to aide in finding the ideal parameters for my xgboost.

As a final model, I used a voting classifier ensemble to classify transactions depending on whether they are fraudulent or not. The purpose of trying these three models was to see which model would give me the best results, the results from the winning model (XGBoost) were then verified using StratifiedKFold specifically to preserve the percentage of samples from each class (frauduluent and non fraudulent).

High Level blog post: https://hackernoon.com/detecting-fraudulent-transactions-88031bac2382

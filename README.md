# Amazon-Food-Product-reviews
Text analysis on reviews of food products available on amazon
# Dataset:  
Number of reviews: 568,454  
Number of users: 256,059  
Number of products: 74,258  
Number of products: 74,258  
Timespan: Oct 1999 - Oct 2012  
Number of Attributes/Columns in data: 10  

# 1. Exploratory data analysis on Amazon fine food reviews dataset.  
   Perform exploratory data analysis on whole data to get some meaningful insights about data.  
   
# 2. Perform text sentimental analysis on Amazon fine food reviews  
There are large number of reviews in the dataset working with such large reviews can run out of memory and system crashes. So we take a sample of 1,00,000 reviews.
Considering only reviews column for text analysis.  
# Featurization  
* Bag Of Words  
* tfidf vectorization  
After featurizing text data with Bag Of Words (BOW)data we got  
1. Train size : 64000 with 28885 Dimensions  
2. CV size : 16000 with 28885 Dimensions  
3. Test size : 20000 with 28885 Dimensions  
After featurizing text data with Tf-Idf data we got  
1. Train size : 64000 with 28885 Dimensions  
2. CV size : 16000 with 28885 Dimensions  
3. Test size : 20000 with 28885 Dimensions  
Y label is sentiment of the review.    
0 for Negative review.  
1 for Positive review.  

Machine Learning Model  
* Naive bayes Model  
* Logistic Regression  
# Preformance of model with F1 score  
Naive bayes Model  
* Bag Of Words => 90.94  
* Tfidf => 90.61  
Logistic Regression  
* Bag Of Words => 93.41  
* Tfidf => 91.90  
# Conclusion
Given data is highly imbalance data with 84% positive and 16% negative score. Taking accuracy as a metric to measure perfomance of the model is a wrong idea because even a dumb model can have an accuracy of 84%. So we take f1 score, precision score and recall score. And also plot connfusion matrix to clearly understand about performance of model.  

1. From all above models we can clearly understand that Logistic regression with Bag of words performs better with f1-score 93%.  
2. If we observe the feature importance (positive and negative words) they are more reasonable and good.  
3. From the confusion matrix we can conclude that more positive lables are mis classified as negative, So False Negative value is high compared to False Positive.  

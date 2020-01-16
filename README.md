# Sentiment-Analysis-on-Amazon-Food-Reviews
### Classifying whether the given food review is either positive or negative.


### Amazon Fine Food Reviews Analysis
Data Source: https://www.kaggle.com/snap/amazon-fine-food-reviews


The Amazon Fine Food Reviews dataset consists of reviews of fine foods from Amazon.

Number of reviews: 568,454
Number of users: 256,059
Number of products: 74,258
Timespan: Oct 1999 - Oct 2012
Number of Attributes/Columns in data: 10

### Attribute Information:

Id
ProductId - unique identifier for the product<br>
UserId - unqiue identifier for the user<br>
ProfileName<br>
HelpfulnessNumerator - number of users who found the review helpful<br>
HelpfulnessDenominator - number of users who indicated whether they found the review helpful or not<br>
Score - rating between 1 and 5<br>
Time - timestamp for the review<br>
Summary - brief summary of the review<br>
Text - text of the review<br>

### Objective:
Given a review, determine whether the review is positive (Rating of 4 or 5) or negative (rating of 1 or 2).

### Loading the data
The dataset is available in two forms.

1.) .csv file<br>
2.) SQLite Database <br>
In order to load the data, We have used the SQLITE dataset as it easier to query the data and visualise the data efficiently.

Here as we only want to get the global sentiment of the recommendations (positive or negative), we will purposefully ignore all Scores equal to 3. If the score id above 3, then the recommendation wil be set to "positive". Otherwise, it will be set to "negative".

### Features used:<br>
Bag of Words<br>
TFIDF vectors<br>
Average Word2vec<br>
TFidf Word2vec<br>

## Conclusion
1.) Random Forrest on Tfidf Vectors gives a AUC of 92.12%<br>
2.) XGBOOST on Tfidf Vectors gives a AUC of of 93% <br>
2.) After running 5 epochs, the model with two LSTM layers gives a accuracy of 92.38%. While the the model with single LSTM layer with 92.4% accuracy. In both cases we get a high accuracy.

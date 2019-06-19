# Problem Statement
To train a classifier to differentiate between two different subreddits from reddit.com

# Executive Summary

### Data Collection
Reddit posts were collected using reddit.com's API. The two selected subreddits are 'love' and 'diet'. 

### Data Cleaning and Exploratory Data Analysis
Rows containing Nan in the 'selftext' column were dropped, leaving a total of 1818 rows from both subreddits. Line splitters and other punctuation were removed and the words were all changed to lower case.

### Preprocessing and Modeling
The reddit comments were tokenized and stop words were removed. Lemmatization was done and the and baseline accuracy of 0.515. This was followed by a train-test-split with stratification. Tf-Idf vectorizer was used with the Naive-Bayes Multinomial classifier resulting in a train score of 0.976 and a test score of 0.963. A second model using count vectorizer and Logisic Regression was done with a train score of 0.989 and a test score of 0.954.  

### Evaluation
The Tf-Idf vectorizer along with the Naive-Bayes Multinomial classifier seems to be the better model due to a higher test score. 

### Conclusions and Recommendations
The Tf-Idf vectorizer along with the Naive-Bayes Multinomial classifier works exceptionally well with the selected subreddits but further testing needs to be done on other subreddits to prevent overfitting. 

# Classification-of-MEPs-Tweets
Classification of MEPs' Tweets
You will investigate a dataset of tweets made by Members of the European Parliament. You will use data collected by Darko Cherepnalkoski, Andreas Karpf, Igor Mozetič, and Miha Grčar for their paper Cohesion and Coalition Formation in the European Parliament: Roll-Call Votes and Twitter Activities (while you are at it, why not read the paper as well?).

This assignment is based on an original assignment by Ioannis Pavlopoulos (postdoc researcher) and Vasiliki Kougia (PhD candidate at AUEB).
# Data Preparation

Get the dataset from https://www.clarin.si/repository/xmlui/handle/11356/1071.

You will use the retweets.csv file.

Keep only the records for which the language of the original tweet is in English.

Get the text of the original tweet and add it to the dataset as an extra column. Use the Tweeter API to get the text (e.g., with Tweepy). In order not to run into rate limits you can ask for multiple tweets with one call.

Keep only the records for which you were able to download the tweet text.

Group the records by the European group of the MEP that posted the original tweet. If you see that there are groups with very few tweets (less than 50), drop them.

# Classification
Train at least two algorithms to learn to classify an unseen tweet. The target variable should be the political party of the original poster and the training features should be the original tweet's text.

You should split your data to training and testing datasets, try the different algorithms with cross validation on the training dataset, and find the best hyperparameters for the best algorithm.

The tweet texts must be converted to a format suitable the classification, bag of word matrices or tf-idf matrices. You must investigate which one gives the best results.

You may want to strip accents, convert everything to lowercase, and remove all English stopwords. In general, you may experiment with additional ideas about how best to tokenize etc.

Report your scores; once you find the best algorithm and the best hyperparameters, report the score on the test data.

To gauge the efficacy of the algorithm, report also the results of a baseline classifier, using, for instance, scikit-learn's DummyClassifier.

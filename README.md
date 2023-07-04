
#  Classification of Depression on Social Media Using Text-Mining

Mental illness has been prevalent in the world, depression is one of the most common psychological problem i know and i would like to help as much as i can. Being a fan of Anthony Bourdain and Robin Williams, It has propel me to explore in this study. With the use of the Large amount of data tweets and Facebook post online i can use machine learning to data mine it and be able to produce a meaningful and useful outcome.

Social media generates countless data every day because of millions of active users share and communicate in entire
community, it changes human interaction. For this project, I will be using Python and various modules and libraries.


## Requirements

Python 3.6.1 or Higher

Twitter developer account

A bunch of modules (Keras, TF, Numpy, sklearns, pandas and itertools)

A lot of patience and a love for machine learning.
## Aim of the Project

The aim of the project is to predict early signs of depression through Social Media text mining. 
## Steps to follow

1.Create a twitter developers account

From that account your would need 4 things.

consumer_key = '', consumer_secret = '', access_token = '', access_secret = ''

2.Using the file "Download_twitter_Api.py" insert the credentials and you can download current tweets using keywords such us depression, anxiety or sadness. When data sets are ready you may proceed on the preprocessing stage. 

	
3.Run "preprocessor.py", This stage will go through your data sets and the given dictionary. The dictionary contain words with their corresponding polarity, which is essential to calcualting the sentiment of each tweet, each word will be seperated, tokenized and given its polarity. Every tweet will consist of the summation of all polarity of each word and devided by number of words in that tweet.


4.Once preprocess is done. You can find the file in the directory "processed_data/output.xlsx". Opening it you will find that the ID (tweet) and Sentiment of each tweet is seperated into 2 columns. With this output you now have a twitter data set and its corresponding sentiment filtered by depress keywords. (Positive, Neutral and Negative)

5.Now for training and Predicting. Make sure all files are located in proper folders, Run "depression_sentiment_analysis.py". The code will run through the output.xlsx file and at the same time recover the tweet corresponding to the id of each sentiment. using this we use the original data and feed them to our classifiers. When everything is done you should have all the AUC of each classifier listed in the console.

But wait, There's more. You will also have the ability to type in a sample tweet, The tweet will go through the highest AUC in the list of classifier to predict the sentiment of the tweet you wrote.


Using the same data set to test my accuracy, I trained and tested about 10,000 Tweets:

AUC is an abbrevation for area under the curve. It is used in classification analysis in order to determine which of the used models predicts the classes best.
## Accuracy

Naive Bayes  Accuracy: 93.79406648429645 

Decision Tree:98.55668748040587 

Support Vector Machine:50.0 

Kneighbors:81.464022923447 

Random Forest: 49.1038137743686 

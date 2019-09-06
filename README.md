# Reddit-Flair-Detection

## PROBLEM STATEMENT:
The task is to build a system that given a link, can detect the flair (category) of a Reddit post.
This task is divided into the following three parts:
#### 1. Data Acquisition
You need to collect the posts from the r/india subreddit. There is no constraint on how many
posts you need to collect, but make sure you have enough posts belonging to each flair on the
subreddit. Try to collect as much data associated with the post as possible (comments, link,
timestamp, user handle). Divide this data into two separate training and testing sets. Save this
data in a MongoDB instance.
#### 2.Flair Detection
Once you have the training and the testing data ready, train a machine learning model to learn
the flair prediction from the features of the posts. You can train multiple models using different
sets of features (title, comment, link) and report the test set accuracy on each one of them.
Please make sure there is no overlap between the training and the testing sets.
#### 3. Web Application
As a final step, we would like you to deploy the code and the trained model as a web application
on Heroku or Digital Ocean Droplet with a user interface where we can input a link to a Reddit
post and your model is used to predict the flair for that post.

## Requirements and Installations
1. Datetime
2. Pandas
3. Praw
4. nltk
5. re
6. numpy
7. Pymongo


## Procedure
##### Data Acquisition



## Data Vectorization
### Bag of Words
Bag of Words (BoW) or CountVectorizer describes the presence of words within the text data. It gives a result of 1 if present in the sentence and 0 if not present. It, therefore, creates a bag of words with a document-matrix count in each text document.
### Vectorizing Data: TF-IDF
It computes “relative frequency” that a word appears in a document compared to its frequency across all documents. 

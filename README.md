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

## Procedure
### Data Acquisition
## (Refer the Jupyter Notebook: Data Scraping.ipynb) 
##### 1.Requirements and Installations
- Datetime
- Pandas
- Praw
- nltk
- re
- numpy
##### 2. Loading the application details and Collecting data for 'India' subreddit
##### 3. Getting the Flairs for Reddit Detection
##### 4. Data Cleaning
- Lower case the data of 'Title','Body','Comments'.
- Replacing the special characters of 'Title','Body','Comments'.
- Remove URLs of 'Title','Body','Comments'.
- Remove Stopwords

## (End result is the csv file named: data_scraped6.csv)

### Flair Detection
## (Refer the Jupyter Notebook: ML-Models.ipynb)
##### 1. Requirements and Installations
- numpy
- pandas
- matplotlib
- sklearn
- pickle
##### 2. Fetch the data and try finding accuracy for various combinations of data 
##### 3. Data Vectorization using Bag of Words
Bag of Words (BoW) or CountVectorizer describes the presence of words within the text data. It gives a result of 1 if present in the sentence and 0 if not present. It, therefore, creates a bag of words with a document-matrix count in each text document.
##### 4. Applying the following models to find the accuracy 
- Logistic Regression
- Linear Discriminan tAnalysis
- K Nearest Neighbours
- Naive Bayes
- SDG
- Random Forest

###### if 'Body' taken a feature
|Model|Accuarcy|Standard Deviation|
|-----|--------|------------------|
|LR   |0.494885|0.075639          |
|LDA  |0.574925|0.106375          |
|KNN  |0.220059|0.069340          |
|NB   |0.499498|0.067077          |
|SDG  |0.491270|0.076233          |
|Rand_Forest|0.494485|0.074110    |

###### If 'title+body+comments' taken as feature
|Model|Accuarcy|Standard Deviation|
|-----|--------|------------------|
|LR   |0.479839|0.070258         |
|LDA  |0.556269 |0.105009          |
|KNN  |0.226272|0.034333          |
|NB   |0.493681|0.067216         |
|SDG  |0.502082|0.085388       |
|Rand_Forest|0.478635|0.069299    |


###### If 'title+body+url_address' taken as feature
|Model|Accuarcy|Standard Deviation|
|-----|--------|------------------|
|LR   | 0.908125|0.021205         |
|LDA  |0.904915 |0.022963          |
|KNN  |0.538011|0.063346          |
|NB   |0.934404|0.014099         |
|SDG  |0.915546|0.023990       |
|Rand_Forest|0.902107|0.019834    |

### References
1. https://machinelearningmastery.com/compare-machine-learning-algorithms-python-scikit-learn/
2. https://praw.readthedocs.io/en/latest/tutorials/comments.html
3. https://towardsdatascience.com/natural-language-processing-nlp-for-machine-learning-d44498845d5b
4. https://towardsdatascience.com/multi-class-text-classification-model-comparison-and-selection-5eb066197568
5. https://www.analyticsvidhya.com/blog/2018/07/hands-on-sentiment-analysis-dataset-python/
6. https://www.analyticsvidhya.com/blog/2018/02/the-different-methods-deal-text-data-predictive-python/


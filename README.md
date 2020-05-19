# Reddit-Flair-Detection

## Procedure
### Data Acquisition
## (Refer the Jupyter Notebook: Data Scraping.ipynb) 
##### 1. Requirements and Installations
- datetime
- pandas
- praw
- nltk
- re
- numpy
##### 2. Loading the application details and Collecting data for 'India' subreddit
##### 3. Getting the Flairs for Reddit Detection
##### 4. Data Cleaning
- Lower case the data of 'Title', 'Body', 'Comments'.
- Replacing the special characters of 'Title', 'Body', 'Comments'.
- Remove URLs of 'Title', 'Body', 'Comments'.
- Remove Stopwords.

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

###### If 'Title+ Body+ Comments' taken as feature
|Model|Accuarcy|Standard Deviation|
|-----|--------|------------------|
|LR   |0.479839|0.070258         |
|LDA  |0.556269 |0.105009          |
|KNN  |0.226272|0.034333          |
|NB   |0.493681|0.067216         |
|SDG  |0.502082|0.085388       |
|Rand_Forest|0.478635|0.069299    |


###### If 'Title+ Comments+ Url_address' taken as feature
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


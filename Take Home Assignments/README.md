Run https://colab.research.google.com/drive/1M-IXzJmzz7zoy0ZpXghz0ZmtJsPR-Bqh?usp=sharing file (Same as Model_Predictions_Pipeline jupyter notebook) to classify unlabelled data as 1- Flagged for Terrorism, 0- Not flagged
* Run the file in Google Colab
* Choose Runtime --> Run all
* Please upload the below files available in the shared folder in the first 4 cells
  * boston_bombing_tweets - Home test Data Scientist: Data provided for the assessment
  * replacements_dict - Consists of dictionary for expanding english contractions
  * important_features_ngrams - Important features based on feature importance
  * boston_bombing_tweets_model - saved final model 
* After all the cells are run, test_data_predictions dataframe produces unlabelled text and their corresponding predictions

Run https://colab.research.google.com/drive/1iUkgW9N6I4wThFBD7_7IXprXoPVfno6T?usp=sharing file (same as Model_Training jupyter notebook) to train labelled data 

Run https://colab.research.google.com/drive/1FXWIeRvk_gI_-8ifmtPnPnZDgaIOzxCv?usp=sharing file (same as Exploratory_Data_Analysis jupyter notebook) to do exploratory data analysis 

### Exploratory_Data_Analysis file consists of analysis of the tweets variable
* Split data into train & test based on the label variable
* Distribution of target variable - balanced data
* Missing value analysis
* Identify duplicates
* Text cleaning: expand english contractions, number of punctuations, hashtags, retweeted or not, URL is present or not, lemmatization of text
* Identfy most common words: uni-grams, bi-grams and tri-grams
* Identify most common hashtags

### Model_Training file consists of preparing the data for model building
* Text data is cleaned and pre-processed
* Labelled data is split into 80% for training and 20% for evaluation

### Model_Predictions_Pipeline files consists of predicting new observations
* Unlabelled data is predicted using the model saved

### Approach
* Started with the analysis of labelled data in boston bombing tweets data file (boston_bombing_tweets - Home test Data Scientist csv file)
* Labelled data has balanced target distribution i.e. equal number of 1s and 0s
* Text cleaning techniques such as converting text to lower case, expanding contractions; removing punctuations, unicode characters, mentions of username, stop words is performed, lemmatization of text is done
* Identfied most frequent hashtags; uni-grams, bi-grams & tri-grams of non-hash words
* Used the frequent words/hashtags to create binary variables or bag of words
* Created other features such as punctuations count, hashtags count, number of words in the text, length of the text, if text is retweet or not, if contains URL or not, etc
* Created baseline model using all the variables created above. Split the labelled data as 80% train and 20% eval. Computed evaluation metrics on eval data after training data using Naive Bayes classification algorithm. This model produced 97.5 accuracy
* Identied important features generated from the above model and used only those features to build another model. This model gave an accuracy of 98.8%
* As Naive Bayes ML algorithm with the above mentioned variables is producing high accuracy, finalized this model and used this model to predict unlabelled text
* Some of the other ways to process text involves utilizing TF-IDT, word embedding techniques such as pre-trained word2vec, GLOVE, ELMo models or senetnce embedding techniques such as Universal Sentence Embedding

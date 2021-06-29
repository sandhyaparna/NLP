Run https://colab.research.google.com/drive/1M-IXzJmzz7zoy0ZpXghz0ZmtJsPR-Bqh?usp=sharing file to classify unlabelled data as 1- Flagged for Terrorism, 0- Not flagged
* Run the file in Google Colab
* Choose Runtime --> Run all
* Please upload the below files available in the shared folder in the first 4 cells
  * boston_bombing_tweets - Home test Data Scientist: Data provided for the assessment
  * replacements_dict - Consists of dictionary for expanding english contractions
  * important_features_ngrams - Important features based on feature importance
  * boston_bombing_tweets_model - saved final model 
* After all the cells are run, test_data_predictions dataframe produces unlabelled text and their corresponding predictions

### Exploratory_Data_Analysis file consists of analysis of the tweets variable
* Split data into train & test based on the label variable
* Distribution of target variable - balanced data
* Missing value analysis
* Identify duplicates
* Text cleaning: expand english contractions, number of punctuations, hashtags, retweeted or not, URL is present or not
* Identfy most common words: uni-grams, bi-grams and tri-grams
* Identify most common hashtags

### Model_Training file consists of preparing the data for model building
* Text data is cleaned and pre-processed
* Labelled data is split into 80% for training and 20% for evaluation

### Model_Predictions_Pipeline files consists of predicting new observations
* Unlabelled data is predicted using the model saved

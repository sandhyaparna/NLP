Run Model_Predictions_Pipeline file to classify unlabelled data as 1- Flagged for Terrorism, 0- Not flagged
* Run the file in Google Colab
* Please upload files by choosing files in the folder
  * boston_bombing_tweets - Home test Data Scientist: Data provided for the assessment
  * replacements_dict - Consists of dictionary for expanding english contractions
  * important_features_ngrams - Important features based on feature importance
  * boston_bombing_tweets_model - saved final model 



* Exploratory_Data_Analysis file consists of analysis of the tweets variable
  * Split data into train & test based on the label variable
  * Distribution of target variable - balanced data
  * Missing value analysis
  * Identify duplicates
  * Text cleaning: expand english contractions, number of punctuations, hashtags, retweeted or not, URL is present or not
  * Identfy most common words: uni-grams, bi-grams and tri-grams
  * Identify most common hashtags

* Model_Training file consists of preparing the data for model building
  * Text data is cleaned and pre-processed
  * Labelled data is split into 80% for training and 20% for evaluation

* Model_Predictions_Pipeline files consists of predicting new observations
  * Unlabelled data is predicted using the model saved






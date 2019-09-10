# Reddit-Flair-Detector

catch it live on https://reddit-flair-detector-final.herokuapp.com/

This is a flask based application hosted on Heroku server.

To execute the application on localhost:
  1. set FLASK_APP = application.py
  2. flask run
  
Description of files used is given below:
  1. templates folder contains all the web templates related to the flask application.
     
     1.1 index.html is home page of application.
     
     1.2 statistics.html contains statistics related to flairs.
     
     1.3 result.html predicts the appropiate flair based on the model.
     
  2. static folder contains all the static images related to flask application.
  3. redditmodelforflair.pkl is the machine learning model used to make flair predictions.
  4. cleaned_reddit_alphabetav5.csv is csv file containing combined features(title+url+comments).
  5. MongoDb collection folder contains the mongodb instance.
  6. requirements.txt specify the requirements for heroku server.
  7. Procfile is the file required by the heroku server.
  8. fetch_data_from_reddit.ipynb gets data from reddit with fields as: flair, title, score, id, url, comms_num, created, body, author,      comments.
  9. reddit_combine_cols.ipynb combines features such as title, url, comments into one.
  10. reddit_stats.ipynb gives statistics on an instance of dataset (it can be viewed in ststistics menu under navigation bar on               application page).
  11. write_combined_features_stopwords_removed.ipynb removes all the STOPWORDS in the dataset using SPACY.
  12. randomforest_on_url.ipynb in this file classifier is applied on dataset using URL as the only feature.
  13. logistic_regression_applied_to_combined_features.ipynb in this file logistic regression is applied to the dataset taking                 (title+url+comments) as combined features and gives a maximum accuracy of 77.90%.
  14. random_forest_on_combined_features.ipynb in this file Random Forest is applied to the dataset taking (title+url+comments) as             combined features and gives accuracy of 74.37%. 

  
Predicted accuracies:  
  
Accuracy given by Random Forest Classifier is 74.372 on combined features when together url,title and comments are used as features.

Accuracy given by Logistic Regression is 77.90 on combined features when together url,title and comments are used as features.

Accuracy of Logistic Regression applied only to url as feature is 60.91.

Accuracy of Random Forest Classifier applied to url is 59.30.

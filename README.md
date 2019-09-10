# reddit-flair-detector

catch it live on https://reddit-flair-detector-final.herokuapp.com/

This is a flask based application hosted on Heroku server.

To execute the application on localhost:
  1. set FLASK_APP = application.py
  2. flask run
  
Descriptioin of files used is given below:
  1. templates folder contains all the web templates related to the flask application.
     1.1 index.html is home page of application.
     1.2 statistics.html contains statistics related to flairs.
     1.3 result.html predicts the appropiate flair based on the model.
  2. static folder contains all the static images related to flask application.
  3. redditmodelforflair.pkl is the machine learning model used to make flair predictions.
  4. cleaned_reddit_alphabetav5.csv is csv file containing combined features(title+url+comments).
  5. MongoDb collection folder contains the mongodb instance and csv.
  6. requirements.txt specify the requirements for heroku server.
  7. Procfile is the file required by the heroku server.
  

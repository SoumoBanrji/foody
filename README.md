# Restaurant Recommender System
## This project is a restaurant recommender system built using Flask web framework, which recommends popular cuisines, popular restaurants, restaurants offering a preferred cuisine, and suggests the ideal price for a dish based on user inputs like location, cuisine, and budget.

![foody_webpage](https://user-images.githubusercontent.com/101920267/232299595-c908c41f-7e1d-47d7-b91a-498f72166ccc.PNG)


### Dependencies
#### Flask
#### Pandas
#### Numpy
#### Pickle
#### bScikit-Learn

#### data/: Contains the datasets used for training the models.
#### saved_model/: Contains the trained models.
#### templates/: Contains the HTML template for the web app.
#### app.py: The Flask application.
#### featureCreation.py: Contains a class to create features from user inputs.
#### modelTraining.py: Contains the code for training the machine learning models.
#### part1.py: Contains functions to extract insights from the data.
#### README.md: The readme file.

## Workflow
### The project workflow can be divided into three parts:

#### 1. Extract insights from data
##### The first part extracts insights from the data using the part1.py file. This part extracts the most popular cuisines, the average price of food per person, the ##### most popular restaurants, and restaurants offering preferred cuisine.

#### 2. Train the models
##### The second part trains the machine learning models using the modelTraining.py file. This part trains two models:

##### A clustering model to cluster restaurants based on their location and price.
##### A regression model to predict the price of a dish based on the cluster label and cuisine.
#### 3. Create features and recommend
##### The third part uses the trained models to create features and recommend restaurants using the app.py and featureCreation.py files.

##### The app.py file is the Flask application that accepts user inputs and renders the output. It calls the FeatureCreator class defined in featureCreation.py to ##### create features from user inputs. It then uses the trained models to predict the ideal price and recommended location.

#### Limitations
##### The models are trained on a limited dataset, and the predictions may not be accurate for all regions.
##### The price recommendations are based on the assumption that the prices are distributed uniformly across all restaurants.
##### The recommendations are based on a single cuisine preference. A multi-cuisine recommendation system could be built by training separate models for each cuisine.

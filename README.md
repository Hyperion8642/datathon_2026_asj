# UW 2026 Datathon Output for Team ASJ 
This repository contains the work done by Team ASJ (Aaron Kann, Saeah Go, and Jason Cao) for the UW 2026 Datathon focused on Accessibility, where we created a machine learning model to classify the severity of an area as less extreme (1,2, or 3) or more extreme (4 or 5), based on the "severity" feature from the Project Sidewalk Seattle Accessibility Dataset. 

## EDA
When conducting EDA, we visualized areas in the city that certain barriers tended to be present, how the severity varied for each barrier, and whether a barrier's temporary nature was relevant. We then drew in external data sources from Seattle's Neighborhood Map (https://data-seattlecitygis.opendata.arcgis.com/datasets/SeattleCityGIS::neighborhood-map-atlas-neighborhoods/explore?location=46.997608%2C-122.705044%2C10) to better visualize barrier patterns (and indirectly, severity patterns) across neighborhoods.

The various EDA and DA files can be seen above. 

## Modelling
When creating a model to predict "severity", we attempted to supplement our data with features from the American Community Survey (https://data-seattlecitygis.opendata.arcgis.com/datasets/SeattleCityGIS::seattle-neighborhoods-top-50-american-community-survey-data.geojson). We used XGBoost models due to their proven ability to classify many features with great accuracy and their ability to visualize the importance of features, logistic regressions, and random forest classifiers. Ultimately, despite our attempts to optimize some of our XGBoost models and our attempts to create a model that could successfully classify all five levels of severity, we decided to stick with a highly accurate random forest model that conducted binary classification due to its stellar performance in its AUC-ROC metric. 

The most relevant file for modelling is: 

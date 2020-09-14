# Disaster Response Application

## Description
The objective of this project is to create a pragmatic application that leverages natural language processing to categorize raw tweets and messages in order to generate an effective triage strategy for disaster response. A dataset is provided us courtesy of Figure Eight. 

The project has 3 parts:
1. ETL pipeline that extracts, cleans and processes data and makes it ready for consumption
2. ML pipeline that categorizes the raw messages delivered by the ETL pipeline.
3. A web application with a basic frontend that produces the model output

## Prerequisites

* Standard Python Distribution 3.5+
* ETL + ML Pipelines: NumPy, SciPy, Pandas, Sciki-Learn
* NLP: nltk
* Database handling: SQLalchemy, pickle
* Frontend: flask, plotly

## File Descriptions
- \
	- README.md
 - ETL Pipeline Preparation.ipynb - guidance on running the ETL pipeline
 - ML Pipeline Preparation.ipynb - guidance on running the ML pipeline including a grid search section
- \app
 - run.py - for running the web app
 - \templates
    - go.html
    - master.html
- \data
   - DisasterResponse.db
   - disaster_categories.csv
   - disaster_messages.csv
   - process_data.py
- \models
   - classifier.pkl : pikle file for the trained model
   - train_classifier.py
## Launch application
 1. Run the following commands in the project's root directory to set up your database and model.

     - To run ETL pipeline that cleans data and stores in database
         `python data/process_data.py data/disaster_messages.csv data/disaster_categories.csv data/DisasterResponse.db`
     - To run ML pipeline that trains classifier and saves
         `python models/train_classifier.py data/DisasterResponse.db models/classifier.pkl`

 2. Run the following command in the app's directory to run your web app.
     `python run.py`

 3. Go to http://0.0.0.0:3001/

## License
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

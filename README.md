# NBA-Project_ML
## Overview
This repository contains code and resources for predicting the NBA Rookie of the Year using machine learning techniques. The project utilizes data from the balldontlie API, spanning from 1979 to the present day.

## Data Collection
### Initial Data Pull
The data collection process begins with pulling historical data from the balldontlie API starting from 1979.
This is done in the notebook First_Pull_Data.ipynb.
### Daily Data Updates
Data is continually updated using a Glue job scheduled to run at 1 AM daily.
The Glue job checks for new data from the previous day's NBA games, deduplicates, and appends it to the historical dataset.
Refer to Glue Job.ipynb for the Glue job implementation.
## Data Processing
Once the data is collected and stored in Amazon S3, it's processed and transformed into Amazon Redshift for further analysis.
Data cleaning and transformation steps are detailed in ROTY Modeling.ipynb.
## Model Training
The project trains a machine learning model to predict the NBA Rookie of the Year using the collected and processed data.
Features are engineered and an SGDClassifier model is trained using Scikit-Learn.
The model predicts the Rookie of the Year for each year using data only from that year, while considering all years for a broader perspective.
Achieved accuracy rate: 76%.
## Libraries Used
Scikit-Learn
Pandas
Numpy
Boto3

## Files
First_Pull_Data.ipynb: Notebook for initial data retrieval from the balldontlie API.
Glue Job.ipynb: Notebook for setting up and scheduling Glue jobs for daily data updates.
ROTY Modeling.ipynb: Notebook for data processing, feature engineering, model training, and prediction of the NBA Rookie of the Year.
## License
This project is licensed under the MIT License.

##Contact
For any inquiries or feedback, feel free to reach out:

Email: minh.trancao30@gmail.com

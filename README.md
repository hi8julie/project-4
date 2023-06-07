# Project 4: Airline Passenger Satisfaction
![shutterstock_1196036986](https://github.com/hi8julie/project-4/assets/118202453/3312c8da-d46d-448b-8806-85515c4f8631)

## Contributors 
* Stephanie Wortman
* Elizabeth Hansen
* Kathryn Kessler
* Julie Eremeeva

## Background 
Michigan-based Airlines – JEKS Air – ran a survey to determine which factors impact passenger satisfaction. 
The data collected includes – 
 * Gender: Gender of the passengers (Female, Male)
 * Customer Type: The customer type (Loyal customer, disloyal customer)
 * Age: The actual age of the passengers
 * Type of Travel: Purpose of the flight of the passengers (Personal Travel, Business Travel)
 * Class: Travel class in the plane of the passengers (Business, Eco, Eco Plus)
 * Flight distance: The flight distance of this journey
 * Inflight wifi service: Satisfaction level of the inflight wifi service (0:Not Applicable;1-5)
 * Departure/Arrival time convenient: Satisfaction level of Departure/Arrival time convenient
 * Ease of Online booking: Satisfaction level of online booking
 * Gate location: Satisfaction level of Gate location
 * Food and drink: Satisfaction level of Food and drink
 * Online boarding: Satisfaction level of online boarding
 * Seat comfort: Satisfaction level of Seat comfort
 * Inflight entertainment: Satisfaction level of inflight entertainment
 * On-board service: Satisfaction level of On-board service
 * Leg room service: Satisfaction level of Leg room service
 * Baggage handling: Satisfaction level of baggage handling
 * Check-in service: Satisfaction level of Check-in service
 * Inflight service: Satisfaction level of inflight service
 * Cleanliness: Satisfaction level of Cleanliness
 * Departure Delay in Minutes: Minutes delayed when departure
 * Arrival Delay in Minutes: Minutes delayed when Arrival
 * Satisfaction: Airline satisfaction level (Satisfaction, neutral or dissatisfaction)

Aside from the overall satisfaction, all other satisfaction metrics are on a scale from 1 to 5.

JESK Air is now asking a team of Data Scientist to help them find an algorithm that could predict customer satisfaction and help the airlines deliver better service.  
The JEKS Air is also interested in building a new set of tools that will allow them to visualize their survey data. They collect a massive amount of data from all over the world each day, but they lack a meaningful way of displaying it. 

## Installation
         # Import our dependencies
         import os
         # Find the latest version of spark 3.x  from http://www.apache.org/dist/spark/ and enter as the spark version
         # For example:
         # spark_version = 'spark-3.3.1'
         spark_version = 'spark-3.3.2'
         os.environ['SPARK_VERSION']=spark_version

         # Install Spark and Java
         !apt-get update
         !apt-get install openjdk-11-jdk-headless -qq > /dev/null
         !wget -q http://www.apache.org/dist/spark/$SPARK_VERSION/$SPARK_VERSION-bin-hadoop3.tgz
         !tar xf $SPARK_VERSION-bin-hadoop3.tgz
         !pip install -q findspark

         # Set Environment Variables
         os.environ["JAVA_HOME"] = "/usr/lib/jvm/java-11-openjdk-amd64"
         os.environ["SPARK_HOME"] = f"/content/{spark_version}-bin-hadoop3"
         from sklearn.model_selection import train_test_split
         from sklearn.preprocessing import StandardScaler
         import pandas as pd
         import tensorflow as tf

         import findspark
         findspark.init() 
         import pyspark
         
         from sklearn.model_selection import train_test_split
         from sklearn.linear_model import LogisticRegression
         
         from sklearn.metrics import confusion_matrix, balanced_accuracy_score, classification_report
         
         from imblearn.over_sampling import RandomOverSampler

## Technologies 
Python Pandas
Tableau
Amazon AWS
Java
PySpark 
TensorFlow
Scikit-Learn

## Data Source 
Kaggle Dataset "Airline Passenger Satisfaction" https://www.kaggle.com/datasets/teejmahal20/airline-passenger-satisfaction

## Initial visualizations
To explore the data before building the ML model, our team has created a Tableau dashboard with high-level findings in the data. Based on the survey, 


## Analysis Report
* The purpose of the analysis is to train and evaluate a model based on passenger satisfaction. 
* The stages of the machine learning process were: 

  - Split the Data into Training and Testing Sets
  - Create a Logistic Regression Model with the Original Data
  - Predict a Logistic Regression Model with Resampled Training Data (to resample the data and achieve a balanced dataset, we used the RandomOverSampler method)
  - Write an Airline Satisfaction Analysis Report

## Results

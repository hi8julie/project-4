# Project 4: Airline Passenger Satisfaction

<img width="352" alt="JEKS pic" src="https://github.com/hi8julie/project-4/assets/118202453/789a9acd-1164-4467-85b0-ab840e60b7c4">



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

JEKS Air is now asking a team of Data Scientist to help them find an algorithm that could predict customer satisfaction and help the airlines deliver better service.  
The JEKS Air is also interested in building a new set of tools that will allow them to visualize their survey data. They collect a massive amount of data from all over the world each day, but they lack a meaningful way of displaying it. 

## Installation
         # Import dependencies
         import os
         import pandas as pd
         import tensorflow as tf
         from sklearn.model_selection import train_test_split
         from sklearn.preprocessing import StandardScaler
         from sklearn.linear_model import LogisticRegression
         from sklearn.metrics import accuracy_score, confusion_matrix, balanced_accuracy_score, classification_report
         from imblearn.over_sampling import RandomOverSampler

         # Install Spark and Java
         !apt-get update
         !apt-get install openjdk-11-jdk-headless -qq > /dev/null
         !wget -q http://www.apache.org/dist/spark/$SPARK_VERSION/$SPARK_VERSION-bin-hadoop3.tgz
         !tar xf $SPARK_VERSION-bin-hadoop3.tgz
         !pip install pyspark
         !pip install -q findspark

         # Set Environment Variables
         spark_version = 'spark-3.4.0'
         os.environ['SPARK_VERSION']= spark_version
         os.environ["JAVA_HOME"] = "/usr/lib/jvm/java-11-openjdk-amd64"
         os.environ["SPARK_HOME"] = f"/content/{spark_version}-bin-hadoop3"

         # Start Spark session
         import findspark
         import pyspark
         findspark.init() 

## Technologies 
* Excel
* Tableau
* Python Pandas
* Python Numpy
* Amazon AWS S3 
* PySpark 
* TensorFlow
* Scikit-Learn
* Google Colab

<img width="660" alt="toolset" src="https://github.com/hi8julie/project-4/assets/118202453/d889d277-694c-4f0a-b30a-22cc537a5b86">



## Data Source 
Kaggle Dataset "Airline Passenger Satisfaction": https://www.kaggle.com/datasets/teejmahal20/airline-passenger-satisfaction

## Initial visualizations
To explore the data before building the ML model, our team has created a Tableau dashboard and Excel charts with high-level findings in the data. 

Tableau Dashboard: https://public.tableau.com/app/profile/elizabeth.hansen5663/viz/AirlineSatisfactionExploration/AirplaneSatisfactionSurveyResults 

<img width="347" alt="dashboard" src="https://github.com/hi8julie/project-4/assets/118202453/f97effd6-da43-4d61-af6a-d50258ce24df">


## Analysis Report
* The purpose of the analysis is to train and evaluate a model based on passenger satisfaction. 
* The stages of the machine learning process were: 

  - Split the Data into Training and Testing Sets
  - Create a Logistic Regression Model with the Original Data
  - Create a Neural Network Model for deep learning
  - Write an Airline Satisfaction Analysis Report

## Results

**Logistic Regression**

<img width="388" alt="report 1" src="https://github.com/hi8julie/project-4/assets/118202453/3d0232e7-b121-42f3-ae74-b07e10c05869">


**Deep Learning**

<img width="495" alt="report 2" src="https://github.com/hi8julie/project-4/assets/118202453/5dddce60-38df-4597-8815-7b7005602126">



## Limitations 
* No data on location and airlines (JEKS AIR was made up by us).
* The answer “neutral” and “dissatisfied” were combined even though they have very different meaning. 
* A lot of  “N/A” inputs. For some columns, keeping N/As was important (e.g., delay in departure/arrival). For other columns, it was unnecessary and might have affected the ML model. 
* We don’t have data on how the survey was run and how representative it is. 




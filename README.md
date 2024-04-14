# Goal : Used Car price - ML Model
Goal of this project is to understand what factors make a car more or less expensive. As a result of this analysis, the project tries to provide clear recommendations to client as to what consumers value in a used car.

To frame the task, throughout our practical applications we will refer back to a standard process in industry for data projects called CRISP-DM. This process provides a framework for working through a data problem. 

## Dataset
The dataset used in this project is the Used Cars Dataset from Kaggle. The provided dataset contains information on 426K cars to ensure speed of processing. 

## Business Understanding
From a business perspective, we are tasked with identifying key drivers for used car prices. The used car business sells used cars from various manufacturers and models and one of the biggest cost is the number of days a used car sits in their inventory. The lower thier 'Days in inventory', the more they make money. Thus the question a used car dealer usually asks what should be their inventory be given there's only so much space they have and need to carfeully choose inventory that will sell fast and lower their 'Days in inventory'. Thier primary goal is to find out what does a custoer want in a used car and that's what this project tries to answer.

## Data Understanding
After considering the business understanding, we want to get familiar with our data. Below are the steps I have taken to understand the historical data.
#1. Identify key attributes of the data (paying more attention to target variable price) such as
<ul>
    <li> missing values </li>
    <li>Null/NaN</li>
    <li>mean</li>
    <li>median</li>
    <li>std. deviation</li>
    <li>distribution</li>
</ul>
#2. Identify categorical columns such as title, Manufacturer, condition, Cylinders etc.
#3. Scan for all columns/attributes of the data set and determine what attributes may not significantly contribute to price. 
#4. Gain more insights about how the data is organized.

## Data Preparation
After our initial exploration and fine tuning of the business understanding, it is time to construct our final dataset prior to modeling. Here, we want to make sure to handle any integrity issues and cleaning, the engineering of new features, any transformations that we believe should happen (scaling, logarithms, normalization, etc.), and general preparation for modeling with sklearn. Below are some of the data cleaning steps taken for the project.


## Analysis
After initial analysis of data,  
## Results
The best model used for this project was a linear regressor with a degree 2 polynomial complexity with a ridge cross validator. Using permutation importance, the following vehicle features were identified as important for predicting the target variable (price):
<ul>
    <li>Odomoeter reading</li>
    <li>Year</li>
    <li>4WD</li>
    <li></li>
</ul>

# Goal : Used Car price - ML Model
Goal of this project is to understand what factors make a car more or less expensive. As a result of this analysis, the project tries to provide recommendations to client as to what consumers value in a used car.

To frame the task, throughout our practical applications I referred back to a standard process in industry for data projects called CRISP-DM. This process provides a framework for working through a data problem. 


## Business Understanding
From a business perspective, we are tasked with identifying key drivers for used car prices. The used car business sells used cars from various manufacturers and models and one of the biggest cost is the number of days a used car sits in their inventory. The lower thier 'Days in inventory', the more they make money. Thus the question a used car dealer usually asks what should be their inventory be given there's only so much space they have and need to carfeully choose inventory that will sell fast and lower their 'Days in inventory'. Thier primary goal is to find out what does a custoer want in a used car and that's what this project tries to answer.

## Data Understanding
<ins>Dataset : </ins>
The dataset used in this project is the used Cars Dataset from Kaggle. The provided dataset contains information on 426K cars to ensure speed of processing.
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
After initial exploration and fine tuning of the business understanding, it is time to construct final dataset prior to modeling. Here, I want to make sure to handle any integrity issues and cleaning, the engineering of new features, any transformations that I believe should happen (scaling, logarithms, normalization, etc.), and general preparation for modeling with sklearn. Below are some of the data cleaning steps taken for the project.

1. The first step was see general info on the data.
2. Next identify value counts by column.
   
![image](https://github.com/NippaniP/Used-Car-Price-Prediction/assets/157237232/743f1588-378a-47af-a258-84b0c53b240c)

3. Based on the count, I had to decide what columns with NaN data can be dropped or filled and what columns can be dropped as they may not have much contribution towards price
4. Below actions were taken:
 <ul>
    <li>Dropped data that has no vales for Size, VIN, condition, cylinder whjere there's no vlaues rows </li>
    <li>Removed 'id', 'region','paint_color','state', 'VIN' from the dataset </li>
    <li>Filled with 'other' for NaN for 'cylinders','title_status' & 'manufacturer' field</li>
    <li>Dropped any other na/NaN rows</li>
</ul>
This is the final clean dataset column counts with.

![image](https://github.com/NippaniP/Used-Car-Price-Prediction/assets/157237232/4bebce09-8c73-4149-8a49-2d5512f7d39e)

5. Next step in data preparation was to identify outliers in the data expecially in price, odometer and year.
6. Starting with Price, it seems the plot below shows a spread indicating outliers
   ![image](https://github.com/NippaniP/Used-Car-Price-Prediction/assets/157237232/aae5a2c3-9b1b-4da1-9ef6-855a0db52c5e)
![image](https://github.com/NippaniP/Used-Car-Price-Prediction/assets/157237232/820bf752-aaee-48f5-be95-efd92b6935c2)

7.I then applied a quintile based approach to remove outliers based on the box plot resulting in a better box plot for price.
![image](https://github.com/NippaniP/Used-Car-Price-Prediction/assets/157237232/2fad33e7-2b17-496a-a9d1-04d239381ee5) ![image](https://github.com/NippaniP/Used-Car-Price-Prediction/assets/157237232/855a48a4-8048-4b31-adf7-458f04e3a72e)



## Modeling
The next step is to apply various regresion models on the data. But first a simple heatmap of correlation matrix was produced to see how the numeric data is related to price.
Below is the heatmap
![image](https://github.com/NippaniP/Used-Car-Price-Prediction/assets/157237232/4a483f58-3836-4540-b31a-7ffa7a0008f8)



## Results
The best model used for this project was a linear regressor with a degree 2 polynomial complexity with a ridge cross validator. Using permutation importance, the following vehicle features were identified as important for predicting the target variable (price):
<ul>
    <li>Odomoeter reading</li>
    <li>Year</li>
    <li>4WD</li>
    <li></li>
</ul>

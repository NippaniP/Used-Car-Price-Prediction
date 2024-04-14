# Goal : Used Car price - ML Model
Goal of this project is to understand what factors make a car more or less expensive. As a result of this analysis, the project tries to provide clear recommendations to client as to what consumers value in a used car.

To frame the task, throughout our practical applications we will refer back to a standard process in industry for data projects called CRISP-DM. This process provides a framework for working through a data problem. 

## Dataset
The dataset used in this project is the Used Cars Dataset from Kaggle. The provided dataset contains information on 426K cars to ensure speed of processing. 

## Business Understanding
From a business perspective, we are tasked with identifying key drivers for used car prices. The used car business sells used cars from various manufacturers and models. The question a used car dealer usually asks what should be their inventory given there's only so much space they have and need to very carfeully choose inventory that will help them sell.

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

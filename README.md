# UCB-AI-ML-PA-II
Practical Assignment #2


What drives the price of car? <img width="978" alt="Screen Shot 2023-11-21 at 1 58 27 PM" src="https://github.com/mzacomp/UCB-AI-ML-PA-II/assets/146776815/20c33fde-8161-4531-b7b5-24dd2a6553ac">

Introduction:
Dataset was found on Kaggle. The dataset contains information on 426K cars. The goal of this assignment is understand the practical factors that contribute to the price of used cars in order to provide useful information for the client, a used cars dealership. This serves as a concise, non-technical review of data analysis and targeted recommendations for the client.


Business Understanding:

Important business objectives after gaining domain knowledge: 

What characteristics make a car more or less attractive to prospective buyers?
How to possibly optimize profit for those car with the valued characteristics?
How to re-strategize marketing to improve sales of cars with these valued characteristics? 


Data Understanding: 

Data was cleaned, meaning NA and unncessary values were dropped to prepare for data analysis. 

<img width="456" alt="Screen Shot 2023-11-21 at 2 18 52 PM" src="https://github.com/mzacomp/UCB-AI-ML-PA-II/assets/146776815/ebe7caeb-8fac-4931-b628-2e03ffd1ed3a">

 Univariate and multivariate data exploration was done. Key visualizations that influenced price are shown below: 


 <img width="893" alt="Screen Shot 2023-11-21 at 2 23 59 PM" src="https://github.com/mzacomp/UCB-AI-ML-PA-II/assets/146776815/a02db54d-8d10-4e90-81d3-fb46e0c1b0c8">

The Linear Regression plot of price and year show an overall increasing trend in car prices over time. 

<img width="793" alt="Screen Shot 2023-11-21 at 2 24 45 PM" src="https://github.com/mzacomp/UCB-AI-ML-PA-II/assets/146776815/25915ff1-fedf-498b-8fe7-0d065ba45a45">

The barplot of car model and price demonstrate that certain models of car are at a higher price.

<img width="857" alt="Screen Shot 2023-11-21 at 2 24 34 PM" src="https://github.com/mzacomp/UCB-AI-ML-PA-II/assets/146776815/e375b9f6-fbde-4094-a5d6-3d3780a6ebc9">

The boxplot of car manufacturers and price demonstrate that certain manfacturers have cars that are at a higher price. 


<img width="815" alt="Screen Shot 2023-11-21 at 2 24 16 PM" src="https://github.com/mzacomp/UCB-AI-ML-PA-II/assets/146776815/866c9162-c33c-4c46-950b-550fae262309">

The bar plot of car type and price demonstrate that certain types of car are at a higher price.


My hypothesis is that year, model, manufacturer, and car type are the most important features/factors in driving car prices. 


Data Preparation:
Data was update to reflect a more modern time period, 2000-2020. Car prices were set for under $40,000 to reflect the current U.S. market for used car prices. Certain unnccessary values were removed in other columns as well. Data was split into training and test data for regression/predictive analysis. 


Modeling: 

Ridge regression and Linear regression models were completed of the training and test datasets, as well as the utilization of GridSearchCV. Necessary column transformers and pipelines were created in order to prepare the analysis for further data evaluation. 

Evaluation: 
R-squared values, training scores, testing scores, test mean squared error, and train mean squared error were computed. The data table below compiles all of this information: 

<img width="699" alt="Screen Shot 2023-11-21 at 2 55 06 PM" src="https://github.com/mzacomp/UCB-AI-ML-PA-II/assets/146776815/710b961a-763c-4052-be2d-56c3dbbf948b">

The data table shows that both regression models had high R-squared values. However, the Linear Regression model had a higher R-squared value of 0.85, which made it the better model to use for further analysis. The R-squared measures the accuracy of how well the data fit into the regression model. A high R-squared value reflects a valuable accuracy measure, which is what was shown in this evaluation. Larger MSE values were expect given the large dataset. 


Feature importance analysis was gathered through acquring the coefficients from the linear regression/GridSearchCV model object. 
![eval_4](https://github.com/mzacomp/UCB-AI-ML-PA-II/assets/146776815/703fa409-4c7d-49c6-8e7e-15300ea9dce3)


The feature importance coefficient bar plot demonstrated that certain car models had higher coefficient values. A permutation feature analysis was performed afterwards to gain further understanding of the most important features. 


![eval_3](https://github.com/mzacomp/UCB-AI-ML-PA-II/assets/146776815/80bfeb09-06e5-499f-b59a-856d0440f005)

The permutation importance bar plot demonstrated that Year, Model, and Odometer were the most important features for price. Year and Model were what I hypothesized to be amongst the most important features. However, odometer was not expected. Manufacturer and car type were fourth and fifth most important feature, respectively. 

Deployment: 

Upon the Evaluation, Model, Year, and Odometer were the important features. My recommendation for the used-car dealership would be to focus on these features for upcoming sales with prospective buyers. I performed another set of data visualizations of these features but within the new time parameterof 2000-2020. 


<img width="772" alt="Screen Shot 2023-11-21 at 4 11 42 PM" src="https://github.com/mzacomp/UCB-AI-ML-PA-II/assets/146776815/1b8cf92c-29c0-4c60-873c-e68c0f05010e">

 These are the current top models for used cars given the new time parameter of 2000-2020.
 

<img width="599" alt="Screen Shot 2023-11-22 at 10 34 17 AM" src="https://github.com/mzacomp/UCB-AI-ML-PA-II/assets/146776815/af5e6cca-ec2b-4899-9ac8-d47c0f40f6d2">

 
Odometer ranges form 0.1-0.25e6 are preferrable.

<img width="838" alt="Screen Shot 2023-11-21 at 4 11 56 PM" src="https://github.com/mzacomp/UCB-AI-ML-PA-II/assets/146776815/d2fd1e65-1cbe-4e7f-9705-657debed10fc">

This linear regression plot clearly demonstrates an upward trend in car price and year. This demonstrates that the need for used cars continue to increase. 

My overall recommendations for the used-cars dealership is to focus on the year and model of the car, as these are the most important features. Secondly, focus on odometer ranges, preferably with a lower range. Marketing efforts should be targeted on these specific features in order to bolster profits and efficiently organize car inventory. These features are most likely what prospective buyers are considering when purchasing a used car.

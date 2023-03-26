# Phase 2 Project

## Project title
Predicting House Prices in King County: A Machine Learning Approach.

## Background
Housing has been a basic human need for centuries, and over time, the concept of housing has evolved with the changing needs and lifestyles of people. Lately, people have commercialized housing aiming at maximum income generation. Different variables however can significantly  impact the overall value of a property in different magnitudes.


##  Project overview
For this project, I will use regression modeling to analyze house sales in a northwestern county.

## Business problem
Homeowners often seek ways to increase the value of their property, and renovations can be an effective way to achieve this. Therefore, there is a need for a reliable way to estimate the impact of home renovations on property value to help homeowners make informed decisions.

## Main objective
* To provide advice to homeowners about how different variables might increase the estimated value of their homes, and by what amount.

## Specific objectives.
* To build a predictive model that can accurately estimate the sale price of houses in King County based on their various features such as number of bedrooms, bathrooms, square footage, location, and others.

* To identify the key features that have the most significant impact on the sale price of houses in King County and provide actionable insights to real estate agents, property developers, and homeowners on how to maximize the value of their properties.

## Data understanding
The King County House Sales dataset contains information on the sale of houses in King County, Washington, USA between May 2014 and May 2015. The dataset includes 21,597 observations and 19 variables. The variables in the dataset include information about the houses, such as the number of bedrooms, bathrooms, and square footage, as well as information about the sale, such as the sale price, date of sale, and condition of the house. There are also variables that describe the location of the house, such as the zip code, latitude, and longitude. The dataset provides a good opportunity to study the factors that affect house prices in the King County area, and to develop predictive models for house prices based on these factors.

The dataset King County House Sales dataset, which can be found in http://localhost:8888/edit/data/kc_house_data.csv in the data folder in this repo.
The data description (column names) are also found in http://localhost:8888/edit/data/column_names.md.

### Libraries
* PYTHON- Programming language
* PANDAS- Exploratory data analysis
* SEABORN- Visualization
* NUMPY - Numerical computing and data analysis
* MATPLOTLIB- Visualization
* STATSMODELS-statistical analysis and modeling
* SCIKIT LEARN- machine learning
* SCIPY- scientific computing
* MATH- basic mathematical operations


## Exploratory data analysis
Distribution for variables in the dataset


![image](https://user-images.githubusercontent.com/122217304/227741879-27e5440d-90cf-4c9e-8363-24437775d51b.png)

Distribution of the dependent variable (price)

![image](https://user-images.githubusercontent.com/122217304/227741924-3173a3ff-cf8d-40dc-a97f-a72d8d83e7e8.png)


A heatmap showing the correlation other variables and themselves. bathroom, sqft_living and grade are highly correlated with a value above .75.this could affect our model.


![image](https://user-images.githubusercontent.com/122217304/227741981-0608b87a-06f2-471d-9d96-058e7347c286.png)


Model one : simple linear regression(price and grade)

![image](https://user-images.githubusercontent.com/122217304/227742048-d43a65b3-5d19-455c-b881-8b668f07e62f.png)


Test for heteroskedasticity. The plot also shows homoscedasticity in our dataset.

![image](https://user-images.githubusercontent.com/122217304/227742086-b5a14285-1606-4f4e-85ea-bbd488c41b3b.png)

Q-Q plot to test for linearity assumption

![image](https://user-images.githubusercontent.com/122217304/227742151-b8be21d5-a3e3-4078-9850-1350a240a335.png)

Correlation between price and the predictor variables

price	     1.000
Sqft_lot	 0.137762
bedrooms	 0.353289
Grade	     0.704877
Bathrooms  0.552219
Floors	   0.313838
Waterfront 0.180529
condition	 0.039044
yr_built   0.081958


Model four : multiple regression

* Train R-squared: 0.6430815463918367 
* Test R-squared: 0.6449536912791446 
* Test set performed better than train. approximately 64.5% of the variance    in the price can be explained by the predictor variables

![image](https://user-images.githubusercontent.com/122217304/227742324-3af7f9b1-ed06-4ba8-b16a-6fc2a397b96e.png)

Model five polynomial regression plot	
* Train set r-squared (training set): 0.6499 	
* Test set r-squared (test set): 0.6527 	
* Test set performed better than train. Approximately 64.5% of the variance in the price can be explained by the predictor variables.

![image](https://user-images.githubusercontent.com/122217304/227742354-19307be0-dcbf-4a35-bb5e-22434a74f1d8.png)


![image](https://user-images.githubusercontent.com/122217304/227742366-a4eefebc-6855-41db-85dd-92dc904af792.png)



## Findings

* Model five is the best model for price prediction in the King County House Sales dataset.

* The grade of the house has the highest correlation with the sale price, with a coefficient of 0.704877. This suggests that higher-quality homes with better overall construction and design tend to command higher prices in the King County housing market.

* The number of bedrooms, bathrooms, and floors also have relatively strong positive correlations with the sale price, with coefficients of 0.353289, 0.552219, and 0.313838, respectively. This indicates that larger and more spacious homes tend to be valued more highly than smaller and less spacious homes.

* The presence of a waterfront property also has a positive correlation with the sale price, although it is relatively weaker than other features, with a coefficient of 0.180529. This suggests that waterfront properties may be considered desirable by some buyers, but they are not universally sought-after and may not always command a significant price premium.

* The year built and condition of the house have relatively weak positive correlations with the sale price, with coefficients of 0.081958 and 0.039044, respectively. This suggests that while newer or better-maintained homes may command slightly higher prices than older or more poorly-maintained homes, these factors are not as important to buyers as other features such as size, quality, and location.


## Recommendations
* Adopting the model from the notebook to predict price using the predictor variables.
* Focus on improving the quality of the house - Given that the grade of the house has the highest correlation with the sale price, homeowners and property developers may want to focus on improving the quality of the home through renovations, upgrades, or better construction materials. This could include installing high-end appliances, upgrading flooring, adding energy-efficient windows or insulation, or redesigning the layout of the home to optimize space.
* Maximize the size and number of bedrooms and bathrooms - The number of bedrooms and bathrooms have relatively strong correlations with the sale price of houses in King County. Homeowners and property developers may want to consider adding additional bedrooms or bathrooms to maximize the value of the home. This could include converting existing space, such as a den or loft, into a bedroom or bathroom, or adding an extension to the house to create more living space.
* Keep the house well-maintained - Although the condition of the house has a relatively weak correlation with the sale price, it is still important to keep the home well-maintained to maximize its value.

## What next?

* Develop an action plan - Once the recommendations have been identified, the next step is to develop a detailed action plan that outlines specific steps to be taken to implement each recommendation.
* Prioritize recommendations - Depending on the available resources and time frame, it may be necessary to prioritize the recommendations in terms of their potential impact and feasibility.
* Monitor and adjust the plan - Once the action plan has been developed and implemented, it is important to monitor the results and make adjustments as needed.
* Evaluate the effectiveness of the recommendations - After the property has been sold, it is important to evaluate the effectiveness of the recommendations and assess whether they had the intended impact on the sale price of the property.








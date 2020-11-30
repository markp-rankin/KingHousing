# KingHousing
##### Flatiron Phase 2 project with Multiple Regression Analysis

## M3 Consulting
##### Our team is composed of Mark Patterson, Matthew Zhang, and Mel Friedman. Our goal is to find affordable housing in Seattle, Washington and the surrounding King County area using predictive data modeling.

## Overview
##### Housing data for King County was provided by Flatiron School which included a little over 20,000 houses sold in 2014 and 2015. This included information such as prices, how many bedrooms and bathrooms, square feet(lot, basement, above ground, living area), the condition of the house and possible views, when it was built and if it was renovated, the zipcode and coordinates, as well as some basic data on the neighborhood. 

##### Our intention is to use our model to help the Salazar family, a family of four, purchase their first home. Their household income is $75,000 and with a down payment of $10,000 they have been approved for a mortgage of $316,000. With the tech boom of the new millennium, and King County being home to tech giants Amazon and Microsoft, the housing market has never been more competitive. We aim to use our model to find the Salazar family a home that meets all their needs and is in their price frame, along with many other hardworking families across king county. 

## Goals
#### 1. Find which features help predict home prices.
  ###### •  What features can be minimized to bring down a home price?
#### 2. Look into housing locations to see if there is any relation to price.
  ###### •  Where in King County have the most affordable houses for new buyers
#### 3. Create an accurate model with low error that includes important features that homeowners want in the price range that they can afford.

## Milestones
### Approach A
##### Created a preliminary model for inference and focused on low and medium priced houses in the range of $154,000 to $605,000. Eventually this was split to just include medium priced homes which further limited the data to $315,000 to $605,000. All seven of the models we created had poor R^2 levels (approximately 0.10). After further EDA we learned that this grouping had poor linearity patterns.

### Approach B
##### Adjusted data to include houses only in our low priced range ($154,000 to $315,000) as well as one-hot encode condition, grade, bedroom, and bathrooms columns. We found that our R^2 score went up, but not by much and only ever got as high as 0.188. 

### Approach C
##### Continued modeling with the dataset used in approach B, but did some transformations on our data. These transformations included getting the log of grade (np.log()) and min-max scaling on the other thirteen predictor variables with the exception of price, yr_built, and yr_renovated. R^2 did not have much significant change and only increased to 0.2. 

### Approach D
##### After not seeing significant changes from data transformations we decided to add more predictor variables related to locational data (latitude, longitude, and zipcode columns). Based on mapping where houses were located and how much they sold for, we could tell that houses sold in southern King County were generally less expensive than houses in the north. Once these predictor variables were added the R^2 went up all the way to 0.492. 

##### We then created 6 bands in equal length for the latitude as well as another 6 bands on 20 year intervals for how old the homes are. After these inclusions we made further adjustments and deleted predictors that had a p-value higher than 0.05 as well as check for mutli-collinearity and delete and conflicting predictors. After these final adjustments, we ended up with an R^2 of 0.518.

## Predictive Modeling

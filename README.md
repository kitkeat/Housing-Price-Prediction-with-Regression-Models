# Problem Statement

Our Client is a Property Agents. They are looking to expand into the Iowa property market. We are tasked to predict the prices of houses based on their characteristics. Our client is also interested in understanding what are the important variables that affects house prices to identify the key characteristics.

**Key Questions from Stakeholder:**
1. Do Neighbourhood matter?
2. Do house size matter?
3. Is a certain area of the house more important?
4. How important is the finishing of the houses?
5. Does the age of the house matter?

# Summary

The lasso regression model was used and it attaied a score of 22664 in the Kaggle competition.

1. The quality and space of the property plays a huge role in the sale price. The increase in the quality means that the material used are also of a higher quality, this is intuitively true with the increase of material used and also the quality of the material will directly impact the price. Since the land is limited, as the livable space increases, the sale price increases.

2. The neighborhood or generally the location of the property affects the sale price.

3. With the increase in quality and total livable area, the price increases.

4. Features extracted from our final model (high coefficient):
    * Above Ground SF (most important)
    * Overall Finishing Score (2nd most important)
    * Basement Finishing + Square Feet
    * Neighbourhood (Greenhill & Stone Bridge)
    * House Age


# Datasets

The following datasets were used for the project:

1. [`train.csv`](./datasets/train.csv): Train data ([source](https://www.kaggle.com/competitions/dsi-us-11-project-2-regression-challenge/data))
2. [`test.csv`](./dataset/test.csv): Test data ([source](https://www.kaggle.com/competitions/dsi-us-11-project-2-regression-challenge/data))

# Data Dictionary

The following data dictionary was extract:

1. [`DataDocumentation.csv`](./dataset/DataDocumentation.csv): Data dictionary ([source](http://jse.amstat.org/v19n3/decock/DataDocumentation.txt))

# Methodology

Linear, Lasso and Ridge regression will be developed to predict the sale price. Out of these 3 models, whichever attained a higher R-squared score will be selected as the final prediction model. Root mean square error will be use to evaluate the accuracy of the model fitting to the validation data points.

Model use:
* Linear Regression
* Lasso Regression
* Ridge Regression

Exploratory Data Analysis:
* Recursive Feature Elimination
* Correlation
* Intuition - reading the data dictionary

Model Evaluation method:
1. R-squared method
2. Root Mean Squared Error


<p>
<img src="images/CA.jpg" width="900" height="574">
</p>


# California Housing Prices Prediction

**Authors**: Ning Chen

The task is to use California census data to build a model of housing prices in the state. This data includes metrics such as the population, median income, and median housing price for each block group in California. Block groups are the smallest geographical unit for which the US Census Bureau publishes sample data. The model will learn from this data and be able to predict the median housing price in any district, given all the other metrics.

## Business Understanding

The model’s output (a prediction of a district’s median housing price) will be fed to another Machine Learning system, along with many other signals. This downstream system will determine whether it is worth investing in a given area or not. Getting this right is critical, as it directly affects revenue.

## Data Understanding


### Exploratory Data Analysis (EDA)

![graph](Images/.png)


### Heatmap

![graph](Images/.png)




## Data Preparation

### Data Cleaning & Feature Engineering

![graph](Images/.png)

The rows with extreme values is considered. Identify categorical variables in the data set and create dummy columns to numeric format through one-hot encoding. New features are generated.

### Interaction Features
Interaction in a non-additive manner when affecting a third variable.

### Multicollinearity

Calculation of correlation and VIF.

![graph](Images/.jpeg)


## Modeling

### Data Split and Normalization
Data is split to training and testing data, and then standardized with respect to normal distribution.

### Linear Regression

![graph](Images/.jpeg)

Fit the model to the training data. Use the model to predict on the training set and the test set. Evaluate the training and test predictions using RMSE. Determine if the model is overfit.

### Non-linear transformations
Polynomial features are implemented to investigate the effect of the non-linear terms.

### Feature Selection Techniques
KBest \
Forward Selection \
RFECV

### Lasso and Ridge
Except ordinary least squares, gradient descent algorithms are also tested.

## Evaluation
The housing prices is predicted for Kings County in Seattle WA. The model solve the problems for pridiction satisfactorily. New features are created to understand the questions. In any of these cases, it is also totally encouraged to revisit the earlier steps to optimze the features and model techniques.

## For More Information

Please review the full analysis in [our Jupyter Notebook]().

For any additional questions, please contact **Ning Chen—chen.ning345@gmail.com**

## Repository Structure

Description of the structure of the repository and its contents:

```
├── README.md                                     <- The top-level README for reviewers of this project
├── Housing Prices Prediction.ipynb               <- Narrative documentation for prediction in Jupyter notebook
├── holdout_features.ipynb                        <- Narrative documentation for holdout in Jupyter notebook
├── CRISP-DM_Housing Prices Prediction.pdf        <- PDF version of project presentation
├── Data                                          <- Both sourced externally and generated from code
└── Images                                        <- Both sourced externally and generated from code

```


## Annotation

Column Names and descriptions for 

* **id** - unique ID for a house
* **date** - Date day house was sold
* **price** - Price is prediction target
* **bedrooms** - Number of bedrooms
* **bathrooms** - Number of bathrooms
* **sqft_living** - square footage of the home
* **sqft_lot** - square footage of the lot
* **floors** - Total floors (levels) in house
* **waterfront** - Whether house has a view to a waterfront
* **view** - Number of times house has been viewed
* **condition** - How good the condition is (overall)
* **grade** - overall grade given to the housing unit, based on King County grading system
* **sqft_above** - square footage of house (apart from basement)
* **sqft_basement** - square footage of the basement
* **yr_built** - Year when house was built
* **yr_renovated** - Year when house was renovated
* **zipcode** - zip code in which house is located
* **lat** - Latitude coordinate
* **long** - Longitude coordinate
* **sqft_living15** - The square footage of interior housing living space for the nearest 15 neighbors
* **sqft_lot15** - The square footage of the land lots of the nearest 15 neighbors

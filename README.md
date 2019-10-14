# Project - Ames Housing Data and Kaggle Challenge


**Primary Objectives:**
1. Creating and iteratively refining a regression model
2. Using [Kaggle](https://www.kaggle.com/) to practice the modeling process
3. Providing business insights through reporting and presentation.

![House](https://thedatasleuth.github.io/static/projects/housing.jpeg)

## Data Overview

1. The Ames Housing Data training set has 82 columns and 2051 rows. testing set has 81 columns and 879 rows. 
2. The variables that we are working with is consist of 23 nominal, 23 ordinal, 14 discrete, and 20 continuous variables. 
3. Ames Housing Data contains all the aspects of a housing. Including but not limited to basement, garage, pool, bedroom, bathroom, constructional material and location. see the full data description in here [data description](http://jse.amstat.org/v19n3/decock/DataDocumentation.txt).

## Data Cleaning and Pre-processing

1. Eliminate the very biased variables. In this project, I defined 'more than 95% of a variable equal to a certain number' as highly biased variables and they won't contains too much information.
2. For continues and discrete variables I did correlation for each variables and housing price. For the variables that have higher than 70% correlation I marked them as must selected numerical variables.
3. For ordinal and nominal data I used their dummy variables to get correlation with housing price. For the variables that their dummy variable has more than 70% correlation I marked them as must selected categorical variables.
4. Selecting additional variables based on bar plot or scatter plot if I saw addition correlation or linear pattern with y variables.
5. Feature engineering:
    - fine_neighbour: if the variables is within the top 4 housing price neighbor
    - poor_neighbour: if the variables is within the bottom housing price neighbor
    - fine_garage_type: if the house is using one of the more expensive type
    - mv: if the house Masonry veneer type is one of the more expensive type
    - garage_finish: if the garage is finished
    - zone1: if the house is in suburb area
    - zone2: if the house is in downtown area 
    - VinylSd1: if the exterior is made from Vinyl Siding
    - Pcnoc: if the foundation is Poured Contrete	
    - reg_lot: if the shape of the house is regular
    - np_bsmt_expo: if the basement has exposure
    - sale_new: is the sale type new.
    - Fence: if house has fence
    - Central Air: if house is using central air
    - bsmtscore: ∑ (basement finish* this finish area)
    - garagescore: ∑(garage finish* this garage area)
    - Low Qual Fin SF: is there unfinished area in the house
    - age: house sold data – house built date 


## The Modeling Process

1. **Linear Regression model**: Linear regression model is the most common model, I used 29 variables as X and housing price as y
2. **Linear Regression model with polynomial features**: I used same 29 variables and used 5 variables for the polynomial features
3. **Lasso model**: Used same 29 variables as X
4. **Ridge model**: Used same 29 variables as X
5. **Model evaluation and select**: 
    - Check residual plot to see are they normally distributed
    - Check cross_val_score for training set and testing  to see are they overfitting

### Organization and Professionalism

**File Structure**
- datasets contains train.csv, test.csv. we build model based on train.csv, and test it on test.csv
- Data Cleaning and pre-processing.ipynb is the data cleaning and pre-processing practics for this data set.
- Modeling.ipynb is the data modeling process. Used 4 model, and evaluated how well each model does and make final model.

The following link is the final presentation of the project[Presentation](https://docs.google.com/presentation/d/115Fi7OnIO-tYzv81MGuR5eRWOAZ8NuO09vgJQzyU5m4/edit#slide=id.g6492462b17_0_824)

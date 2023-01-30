# Overview

Using a dataset of over 34,000 organizations that were funded by a fictitious charity named Alphabet Soup, machine learning techniques and neural networks were used to predict whether or not future applicants would be successful if they received funding.

# Results

## Data Preprocessing
* The target variable for this model is the "IS_SUCCESSFUL" column, which indicates whether or not an organization was successful after receiving funding from Alphabet Soup.
* Prior to processing the data the "NAME" and "EIN" columns were removed, as identificaiton data was deemed an unneccessary variable for predicting success.
* Two columns ("APPLICATION_TYPE" and "CLASSIFICATION") were evaluated for the number of responses at each value. Rare values were binned and labeled "Other" to prevent outliers from skewing the results.

## Compiling, Training, And Evaluating The Model




# Summary

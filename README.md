# Overview

Using a dataset of over 34,000 organizations that were funded by a fictitious charity named Alphabet Soup, machine learning techniques and neural networks were used to predict whether or not future applicants would be successful if they received funding.

# Results

## Data Preprocessing
* The target variable for this model is the "IS_SUCCESSFUL" column, which indicates whether or not an organization was successful after receiving funding from Alphabet Soup.
* Prior to processing the data, the "NAME" and "EIN" columns were removed, as identificaiton data was deemed an unneccessary variable for predicting success.
* Two columns ("APPLICATION_TYPE" and "CLASSIFICATION") were evaluated for the number of responses at each value. Rare values were binned and labeled "Other" to prevent outliers from skewing the results.
* Columns with categorical data ("APPLICATION_TYPE", "AFFILIATION", "CLASSIFICATION", "USE_CASE", "ORGANIZATION", "INCOME_AMT", and "SPECIAL_CONSIDERATIONS") were encoded using OneHotEncoder and converted to numerical data.

## Compiling, Training, And Evaluating The Model
* The neural network contained 2 hidden layers (the first with 80 neurons and the second with 30 neurons) which were both processed with the "Relu" activation function. The output layer utilized the "Sigmoid" activation function.

<p align="center"><img width="550" alt="nn_features" src="https://user-images.githubusercontent.com/111674383/215394631-8ac5e902-9083-4194-bcc7-d825bfc3f596.png"></p>



# Summary

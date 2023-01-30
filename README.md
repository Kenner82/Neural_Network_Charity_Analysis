# Overview

Using a dataset of over 34,000 organizations that were funded by a fictitious charity named Alphabet Soup, machine learning techniques and neural networks were used to predict whether or not future applicants would be successful if they received funding.

# Results

## Data Preprocessing
* The target variable for this model is the "IS_SUCCESSFUL" column, which indicates whether or not an organization was successful after receiving funding from Alphabet Soup.
* Prior to processing the data, the "NAME" and "EIN" columns were removed, as identification data was deemed an unnecessary variable for predicting success.
* Two columns ("APPLICATION_TYPE" and "CLASSIFICATION") were evaluated for the number of responses at each value. Rare values were binned and labeled "Other" to prevent outliers from skewing the results.
* Columns with categorical data ("APPLICATION_TYPE", "AFFILIATION", "CLASSIFICATION", "USE_CASE", "ORGANIZATION", "INCOME_AMT", and "SPECIAL_CONSIDERATIONS") were encoded using OneHotEncoder and converted to numerical data.

## Compiling, Training, And Evaluating The Model
* The neural network contained 2 hidden layers (the first with 80 neurons and the second with 30 neurons) which were both processed with the "Relu" activation function. The output layer utilized the "Sigmoid" activation function.

<p align="center"><img width="550" alt="nn_features" src="https://user-images.githubusercontent.com/111674383/215394631-8ac5e902-9083-4194-bcc7-d825bfc3f596.png"></p>

* The current model was unable to reach the target 75% accuracy.

<p align="center"><img width="550" alt="loss_accuracy" src="https://user-images.githubusercontent.com/111674383/215395549-e0d2db34-e4a5-4b50-a488-8af1cb56b7a5.png"></p>

* Numerous steps were taken to try and increase the target model performance, alone and in various combinations with one another.
  * "INCOME_AMT" and/or "ASK_AMT" columns were dropped
  * The cut-off values for binning "APPLICATION_TYPE" and/or "CLASSIFICATION" were increased and decreased
  * The number of hidden layers were increased and decreased, with values ranging from 1-4
  * The number of neurons in each layer were increased and decreased, with values ranging from 1 - 100
  * The output layer activation was tested using "Relu" and hidden layer activations were tested with "Sigmoid"
  * Number of epochs was increased and decreased, ranging from 50-250

* While some feature combinations decreased accuracy by less than 1%, none of them increased the model performance to the target value.

# Summary
Future attempts to increase model performance could include addressing the "INCOME_AMT" column. The majority of responses are listed as "0", which does not fall into any reasonable range. There is also no bucket to incorporate the 500,000-1M range. Whether or not it is possible to reconfigure the currently available data, this could be addressed when collecting data moving forward.

<img width="500" alt="income" src="https://user-images.githubusercontent.com/111674383/215398494-60538eaf-8af4-4f6a-bb1b-30eabf08b8aa.png">

Additionally, a random forest model could be attempted and compared to the results achieved with the neural network.

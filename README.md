# Neural_Network_Charity_Analysis
Using machine learning and neural networks, we'll use the features in a provided dataset to help create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup.

## Overview of the Analysis

The features provided in Alphabet Soup is used to create a binary clasifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup. The dataset includes more than 34,000 organizations that have recieved funding from Alphabet Soup over the years.

COLUMNS:

- EIN and NAME—Identification columns
- APPLICATION_TYPE—Alphabet Soup application type
- AFFILIATION—Affiliated sector of industry
- CLASSIFICATION—Government organization classification
- USE_CASE—Use case for funding
- ORGANIZATION—Organization type
- STATUS—Active status
- INCOME_AMT—Income classification
- SPECIAL_CONSIDERATIONS—Special consideration for application
- ASK_AMT—Funding amount requested
- IS_SUCCESSFUL—Was the money used effectively

## Results

### Data Preprocessing 

- What variable(s) are considered the target(s) for your model?

  - The target labeled "IS_SUCCESSFUL" - This assesses how effectively the money was used.

- What variable(s) are considered to be the features for your model?

  - Features are all one-hot encoded variables (encoded from object and/or string variables), and int64 variables. These incude items such as the application type, classification, organization, income amount, etc.

- What variable(s) are neither targets nor features, and should be removed from the input data?

  - Removed the catergorical variable lists that dtype = objects. Objects variable are neither targets nor features. For future models, consider removing STATUS, SPECIAL CONSIDERATIONS, and ASk_AMT as the data suggests they do not overall improve the network.

  ### Compiling, Training, and Evaluating the Model

A series of attempts were made to try to get the model up to 75%. The following describes the intent made:

- First, an attempt was made to change the neurons values, add hidden layers, and change activation functions. The neuron value was increased to 100 units for layer one, which resulted in a model accuracy of. 

- Next, hidden layers with neuron units = 10 were added, and the `relu` was used as the activation function. The accuracy looks about the same at .

- The following attempt changed the activation function of the hidden layers that provided minimal improvement. The accuracy is now at . 

- The last attempt set the first hidden layers with units = 6, and activation funcions as `tanh`. The second hidden layer were set at units = 6, and the activation functions as `relu`. The third hidden layer with units = 3, and activation functions as `relu`. The accuracy and loss improved marginally and remains at .

## Summary








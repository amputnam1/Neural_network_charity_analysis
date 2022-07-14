# Neural_network_charity_analysis

## Overview
The goal of this project is to create a binary classifier using a neural network and strive to predict if an applicant to a charity organization (by the name of Alphabet for this use case) will be successful in their funding. The dataset was in the form of a csv file including 34,000 organizations who received funding from Alphabet Soup.

The tools and libraries used include the following:

- Scikit-learn
- Pandas
- Tensorflow

Columns included the following: 

- EIN and NAME — Identification columns
- APPLICATION_TYPE — Alphabet Soup application type
- INCOME_AMT — Income classification
- AFFILIATION — Affiliated sector of industry
- USE_CASE — Use case for funding
- ORGANIZATION — Organization type
- STATUS — Active status
- CLASSIFICATION — Government organization classification
- SPECIAL_CONSIDERATIONS — Special consideration for application
- ASK_AMT — Funding amount requested
- IS_SUCCESSFUL — Was the money used effectively

## Results

### Preprocessing
The first part of the assignment was to examine and preprocess the dataset included in the module using the target variable of IS_SUCCESSFUL column, and the unnecessary data for the model was EIN and NAME columns. All of the other columns were still included in the model.

From here, the steps were to bin, encode, and scale the data.

Note that any APPLICATION_TYPE with less than 1,000 was put into OTHER. Also, the object type columns were encoded with Onehotencoder. The SPECIAL_CONSIDERATIONS_N columm was removed given that it was duplicative of SPECIAL_CONSIDERATIONS_Y. Also, the columns were all scaled using the Standard Scaler. 

### Compiling, Training and Evaluating


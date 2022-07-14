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
For the first model I used two layers, one with 80 neurons, the second with 45 neurons which was a total of 6,891 and trainable parameters.

The layers each had relu activation functions.

The output layer used sigmoid activation function. Though this only helped me in getting a 72.6% accuracy which wasn't ideal. 

There were other models that I used trying to strive for at least 75% accuracy. In the following attempts I tried the following: binning Income_AMT values that wer emore than 5 million into the 5m bin, added a third hidden layer, increased the number of the trainable parameters to 9,411. Also, anothe rmethod I incorporated in attempt to reach the 75% accuracy was to increase the training epochs from 100 to 150, then to 300. Another tactic was when compiling the model and using the adamax as well as the nadam optimizers. In addition to that I tried using the tanh activation function for the hidden layers. Tjhen finally, unbinned various values by lowering the threshold from 1000 to 700 values for the application_type as well as CLASSIFICATION. 

## Summary
Despite my attempts I was unsuccessful in raising the models accuracy to above 73% to the goal of 75%. As you can see above through the desciption, I tried multiple methods and experiments when attempting to inprove the accuracy of the models. For instance, increasing the parameters and training epochs wasn't successful in helping me reach my goal. In the future, I would hope that I would have more time, peers who I can lean on for support, or within a work environment or organization with historical data and examples of past experiments and findings that I can learn from and adopt to scale further to projects such as this one. 

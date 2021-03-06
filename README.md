# Overview
Alphabet Soup is a foundation that funds agencies, impacting the community. This project creates a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup.

# Results
**Data Preprocessing**
\
The data consists of a CSV file, containing more than 34,000 organizations that have received funding from Alphabet Soup over the years. Within this dataset are a number of columns that capture metadata about each organization: 
\
EIN and NAME—Identification columns
\
APPLICATION_TYPE—Alphabet Soup application type
\
AFFILIATION—Affiliated sector of industry
\
CLASSIFICATION—Government organization classification
\
USE_CASE—Use case for funding
\
ORGANIZATION—Organization type
\
STATUS—Active status
\
INCOME_AMT—Income classification
\
SPECIAL_CONSIDERATIONS—Special consideration for application
\
ASK_AMT—Funding amount requested
\
IS_SUCCESSFUL—Was the money used effectively
\
\
To optimize the model, the analysis drops noisy variables, such as EIN, NAME, AFFILIATION, SPECIAL_CONSIDERATIONS.
\
\
**Compiling, Training, and Evaluating the Model**
\
The artificial neuron network (ANN) represents a set of layers: input, hidden, and output. This model uses 35 neurons in the input layer, because the input layer equals the number of input variables in the data. The number of outputs associated with each input determines the number of neurons in the output layer. Since the data must be separated non-linearly, the ANN employs hidden layers. Trial and error reveals that 3 hidden layers help to set the best decision boundary. 
\
\
Weights and biases characterize a system of connections, which supports processing in the hidden layers. This model creates a callback that saves weights every 5 epochs. When the input is received, the neuron calculates a weighted-sum and adds the bias. According to the result and the pre-set activation function (sigmoid), the model decides whether or not to run. Afterwards, the neuron transmits the information downstream. Finally, the last hidden layer links to the output layer, and the outputlayer generates one neuron for each possible desired output.
\
Unfortunately, this model did not achieve the target performance of 75%. However, dropping variables and adding a hidden layer increased the accuracy from 49% to 66%.

# Summary
To continue improving the model, the next iteration should alter the number of neurons, set-up of the weights, and amount of data. The accuracy of a model measures of how accurate your model's prediction is compared to the true data. The best version of this model had an accuracy of 66%, so there is still room for improvement.
\
\
A logistic regression model could alternatively address Alphabet Soup's problem of what agencies to fund. A logistic regression is a classification algorithm that analyzes continuous and categorical variables. Using a combination of input variables, logistic regression predicts the probability of the input data belonging to one of two groups. If the probability is above a predetermined cutoff, the sample is assigned to the first group, otherwise it is assigned to the second. For example, using the agencies' information (such as ASK_AMT and IS_SUCCESSSFUL), logistic regression could be used by a Alphabet Soup to determine if the agency does or does not qualify for a grant.

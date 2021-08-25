# Neural_Network_Charity_Analysis

## Overview: 

The purpose of this analysis is to use Nueral Networks to try to predict if a proposals are likely to be successful. This is accomplished using Tensor Flow's Keras to train and test existing data.

## Results:

### Data Preprocessing:

* The "IS_SUCCESSFUL" column is the target of the data. This columm gave the result of whether a proposal was successful.

* "APPLICATION_TYPE", "AFFILIATION", "CLASSIFICATION", "USE_CASE", "ORGANIZATION", "STATUS", "INCOME_AMT", "SPECIAL_CONSIDERATIONS" and "ASK_AMT" are all considered features for this model. "SPECIAL_CONSIDERATIONS" was later removed as a feature.

* Two variables "EIN" and "NAME" were neither targets nor features, and were removed from the input data.

### Compiling, Training, and Evaluating the Model
* How many neurons, layers, and activation functions did you select for your neural network model, and why?
The original model had the input layer with 80 nodes, then a hidden layer with 30 nodes, and an output layer with 1 node. The input and hidden layers used the Relu activation, and the output has a sigmoid. The final version had 100 nodes, and two hidden layers 60 and 30 nodes each.

* Were you able to achieve the target model performance?
I was not able to achieve the performance of 75%

* What steps did you take to try and increase model performance?
removed the special considerations. batched the affiliation. Added an extra hidden layer. Changed number of nodes, changed batching for application and classification.

## Summary: 
The model, even with the different optimizations did not achieve more than 74%. A possible different model to use.
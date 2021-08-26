# Neural_Network_Charity_Analysis

## Overview: 

The purpose of this analysis is to use Nueral Networks to try to predict if a proposals are likely to be successful. This is accomplished using Tensor Flow's Keras to train and test existing data.

## Results:

### Data Preprocessing:

* The "IS_SUCCESSFUL" column is the target of the data. This columm gave the result of whether a proposal was successful.

* "APPLICATION_TYPE", "AFFILIATION", "CLASSIFICATION", "USE_CASE", "ORGANIZATION", "STATUS", "INCOME_AMT", "SPECIAL_CONSIDERATIONS" and "ASK_AMT" are all considered features for this model. "SPECIAL_CONSIDERATIONS" was later removed as a feature.

* Two variables "EIN" and "NAME" were neither targets nor features, and were removed from the input data.

### Compiling, Training, and Evaluating the Model
1. How many neurons, layers, and activation functions did you select for your neural network model, and why?
* The original model had the input layer with 80 nodes, then a hidden layer with 30 nodes, and an output layer with 1 node. The input and hidden layers used the Relu activation, and the output has a sigmoid. 
* Optimization 1: Input layer: 80 nodes - relu; 2 hidden layers with 40 and 20 nodes - relu; an output layer with 1 node - sigmoid.
* Optimization 2: Input layer: 60 nodes - relu; 2 hidden layers with 45 - relu and 30 - tanh nodes; an output layer with 1 node - sigmoid.
* Optimization 3:The final version had and input layer with 100 nodes - relu; and three hidden layers 80-relu, 40-relu, and 20-tanh nodes each; an output layer with 1 node - sigmoid.

2. Were you able to achieve the target model performance?
* I was not able to achieve the performance of 75%; even with the optimizations it stayed just under 75%.

3. What steps did you take to try and increase model performance?
* Removed the Special Considerations column. 
* Btched the affiliation column. 
* Added extra hidden layers. 
* Changed number of nodes in input and hidden layer nodes. 
* Changed batching groups for the Application and Classification columns.

## Summary: 
The model, even with the different optimizations did not achieve more than 74%. A possible way to try to improve the model would be to use the keras tuner. Allow it to run different combinations of layers, nodes, and activations.
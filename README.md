# charity-funding-predictor

This repository contains a machine learning model attempting to determine if the nonprofit foundation Alphabet Soup can choose applicants to fund with high chances of success. A neural network machine learning model was designed using a dataset from Alphabet Soup applicants and trained with a goal of 75% accuracy.

## Technologies

- Python
- Pandas
- Jupyter Notebook
- Sci-kit Learn
- Tensorflow

## Report

### Overview

This analysis was performed to attempt to optimize the model to atleast 75% accuracy at predicting successful applicants

### Results

#### Data Preprocessing

- The target variable for the model was determined to be the "IS_SUCCESSFUL" column
- The features used to train the model were the remaining columns minus a couple of columns that were removed which is explained below
- The "EIN" and "NAME" columns were removed since they provided no numerical data and were simply identifying columns

#### Compiling, Training and Evaluating the Model

- My baseline model was designed using 3 different layers (2 hidden and 1 output layer). The hidden layers used the relu activation function and had 80 and 30 neurons while the output layer used sigmoid activation function with 1 neuron.
- This initial model was just under the intended 75% accuracy.
  ![baselineModel](/Images/Original_setup.png)
- 3 different attempts were made to increase the accuracy but none of them were considered a success with no-minimal accuracy improvement

1. Dropped ASK_AMT column to limit the number of variables in the dataset
   ![attempt1](/Images/Optimization_attempt1.png)
2. Added another hidden layer with 30 neurons
   ![attempt2](/Images/Optimization_attempt2.png)
3. Tried the tanh activation function instead of the relu activation function
   ![attempt3](/Images/Optimization_attempt3.png)

### Summary

Overall the designed model was close to the intended accuracy benchmark of 75% but did not not quite reach it. The optimization of the model was not successful and I am not sure what other methods could be used to increase it over the 75% threshold. Perhaps using a simpler classification model like the RandomForestClassifier would be more successful.

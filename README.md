# Neural_Network_Charity_Analysis
## Overview
### Purpose
The purpose of this anaylsis was to create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup. Ideally this binary clasifier would have a high accuracy rate in order to help the foundation predict where to make investments.
### Tools/Resources
* Jupyter Notebook 6.0.3
* Python 3.7.9
* Anaconda 4.9.2
* scikit-learn library
* Tensorflow
* Charity dataset `charity.csv`

## Results
### Data Prepocessing
* The target for the model (i.e. y) is the `IS_SUCCESSFUL` column
* The X or the features for the model were: `APPLICATION_TYPE`, `AFFILIATION`, `CLASSIFICATION`, `USE_CASE`, `ORGANIZATION`, `STATUS`, `INCOME_AMT`, `ASK_AMT`, `SPECIAL_CONSIDERATIONS`
* `EIN` and `NAME` columns were deleted from features because they ware non-beneficial. They would be useless to the model

### Compiling, Training, and Evaluating the Model
* In the orginial model, I used 2 hidden layers, 80 neurons in the 1st layer, 30 in the 2nd, used the relu activation for the inputs and sigmoid for the output. I chose this format because of the amount of data and features involved. 1 hidden layer most likely would not result in a very accurate model and having too many could overfit the model, so it's best to just start with two layers. Relu and sigmoid were used because they are useful for classification and sigmoid is ideal for binary classification
* I was not able to achieve the target model performance of > 75% accuracy. 
* To increase the model performance, I took the model and made alterations in the `AlphabetSoupCharity_Optimzation.ipynb` file. For the first optimization (nn), i increased the number of hidden layers to 3, with the third hidden layer having 12 neurons. 
* For the second optimization(nn2), I increased all the neurons in each of the hidden layers to 95, 45, 30, respectively. Accuracy was 73% 
* For the third optimization (nn3), I changed all the activation functions from relu and sigmoid to tanh. 

### Summary
* For my original model, my accuracy was 72.7% 
* For for first optimization, the accuracy was 73.1%
* nn2 accuracy was 73.0%
* nn3 accuracy was 73.0%
* A random forest model may be ideal in this situation because it would combine smaller models to make a more robust model and it is ideal for such tabular data.
* Anoather suggestion would be to take out the `STATUS` column if we wanted to continue to use a neural network.

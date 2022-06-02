# Neural Network Models

## Overview:
Create a binary classifier that is capable of predicting whether applicants will be successful if funded by the 'Alphabet Soup' Charitable Organization.

## Results:

### Data Preprocessing
1. The target variable for our model is the `IS_SUCCESSFUL` variable.
2. The following variables were used as features in our model:
    - `APPLICATION_TYPE`
    - `AFFILIATION`
    - `CLASSIFICATION`
    - `USE_CASE`
    - `ORGANIZATION`
    - `STATUS`
    - `INCOME_AMT`
    - `ASK_AMT`
3. The `EIN`, `NAME` and `SPECIAL_CONSIDERATIONS` variables were excluded from our input data.


### Compiling, Training, and Evaluating our Model
1. In our first model, we used two hidden layers as a starting point. 
    - In the first layer, we used 80 neurons which is roughly twice the number of inputs, and in the second layer, we used 30 neurons (generally expected to be less than the first layer. 
    - For the two hidden layers, We used the 'relu' activation function which is ideal for looking at positive nonlinear input data for classification (as well as regression).
    - For the output layer, we used the 'sigmoid' function, which normalizes values to a probability between 0 and 1 (ideal for binary classification).
2. Our target model performance was 75% - while we did not achieve this, we did take several steps to improve our model's accuracy.
    - <u>**MODEL 1**</u>: In our first attempt to optimize, we tried excluding the `SPECIAL_CONSIDERATIONS` variable from our input data, and also added a third hidden layer to our model with 5 neurons. This gave us an Accuracy score of 72.8%

    - <u>**MODEL 2**</u>: In our second attempt, we used 100 Epochs (rather than 50) to see if the model's performance would improve over more iterations. We also tested the Tanh activation function on the output layer. The resulting accuracy score was 72.7% which indicated to us that the Sigmoid activation function was actually preferred over the Tanh function. 

    - <u>**MODEL 3**</u>: In our final attempt, we reverted the output layer's activation function back to Sigmoid, and instead increased the number of neurons across all layers (with 120 in layer 1 roughly equating to 3x the number of inputs), and again increased our number of Epochs (to 200). This brought our accuracy score up to 72.9%

## Summary:
Overall, our deep learning (neural network) model performed with ~72-73% accuracy. While neural network models are very powerful and can handle all sorts of data types and structures, they are sometimes difficult to train. An alternative to using a neural network model would be to use Random Forest classifier model, which is a type of ensemble learning model that combines multiple smaller models. The Random Forest Classifier model is much simpler to code, but performs comparably to deep learning models in many cases.

## Tools
1. Python (Jupyter Notebook)
    - sklearn 
    - pandas
    - tensorflow

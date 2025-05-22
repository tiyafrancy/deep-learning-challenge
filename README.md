# Report on the Neural Network Model for Alphabet Soup

## Overview of the Analysis

The purpose of this analysis is that the nonprofit foundation Alphabet Soup, wants a tool that can help it select the applicants for funding with the best chance of success in their ventures. With the knowledge of machine learning and neural networks, we’ll use the features in the provided dataset to create a binary classifier that can predict whether applicants will be successful if funded by Alphabet Soup.

## Results

* Data Preprocessing
        
  + Target Variable
    - **IS_SUCCESSFUL** : was the money used effectively (1 for successful, 0 for unsuccessful)
      
  + Feature Variables
    - **APPLICATION_TYPE** : Alphabet Soup application type
    - **AFFILIATION** : Affiliated sector of industry
    - **CLASSIFICATION** : Government organization classification
    - **USE_CASE** : Use case for funding
    - **ORGANIZATION** : Organization type
    - **STATUS** : Active status
    - **INCOME_AMT** : Income classification
    - **SPECIAL_CONSIDERATIONS** : Special considerations for application
    - **ASK_AMT** : Funding amount requested

  + Removed Variables
    - **EIN and NAME** : Identification columns; should be removed from the input data because these variables do not contribute to the prediction.

 * Compiling, Training, and Evaluating the Model

   + First Model
     - Input Layer: The model has an input layer that corresponds to the number of features in the dataset, which is determined by num_input_features.
     - Hidden Layer 1: 80 neurons with a **relu** activation function.
     - Hidden Layer 2: 30 neurons with a **relu** activation function.
     - Output Layer: 1 neuron with a **sigmoid** activation function for binary classification.
     - Model Performance
                The model achieved an accuracy of approximately 72.96% on the test dataset, with a loss of 0.5578. This indicates that the model is performing reasonably well, but fails to achieve a target predictive accuracy higher than 75%.

   + Second Model
     - Input Layer: The model takes in features from the dataset, with the number of input features determined by X_train_scaled.shape[1]
     - Hidden Layer 1: 120 neurons with a **relu** activation function
     - Hidden Layer 2: 60 neurons with a **relu** activation fuction
     - Hidden Layer 3: 30 neurons with a **relu** activation function
     - Output Layer: 1 neuron with a **sigmoid** activation fucntion for binary classification.
     - Model Performance
               The model achieved an accuracy of approximately 72.94% and a loss of 0.5551 on the test dataset. Adding a new hidden layer does not make any significant improvement in the result.
  
   + Third Model
     - Input Layer: The model takes in a number of input features equal to num_input_features, which is determined by the shape of the scaled training data.
     - Hidden Layer 1: 128 neurons with a **tanh** activation function
     - Hidden Layer 2: 64 neurons with a **tanh** aactivation function
     - Hidden Layer 3: 33 neurons with a **tanh** activation function
     - Output Layer: 1 neuron with a **hard_sigmoid** activation function
     - Model Performance
               The model achieved an accuracy of approximately 73.07% and a loss of 0.5548 on the test dataset. Changing the activation function imporoves the results slightly, but not able to achieve the target performance, which is above 75%.

  + Fourth Model
     - Input Layer: The model has an input layer that corresponds to the number of features in the dataset, which is determined by num_input_features.
     - Hidden Layer 1: 10 neurons with a **leaky_relu** activation function
     - Hidden Layer 2: 20 neurons with a **leaky_relu** aactivation function
     - Hidden Layer 3: 30 neurons with a **leaky_relu** activation function
     - Output Layer: 1 neuron with a **sigmoid** activation function
     - Model Performance
               The model achieved an accuracy of approximately 73.26% and a loss of 0.5507 on the test dataset. Changing the activation function imporoves the results slightly, but not able to achieve the target performance, which is above 75%.

* Steps Taken to Increase Model Performance
  

    

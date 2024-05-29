---

## Overview of the Analysis

The purpose of this analysis is to develop a deep learning model capable of predicting the success of charity donation applications using the provided dataset. By preprocessing the data, constructing, training, and optimizing a neural network, the goal is to create a model that can accurately classify applications as successful or unsuccessful. This analysis involves multiple stages, including data cleaning, feature engineering, and model optimization to achieve the target accuracy of 75%.

## Results

### Data Preprocessing

- **Target Variable**: 
  - `IS_SUCCESSFUL`: This variable indicates whether a charity donation application was successful.

- **Feature Variables**: 
  - `APPLICATION_TYPE`
  - `AFFILIATION`
  - `CLASSIFICATION`
  - `USE_CASE`
  - `ORGANIZATION`
  - `STATUS`
  - `INCOME_AMT`
  - `SPECIAL_CONSIDERATIONS`

- **Removed Variables**: 
  - `EIN` and `NAME`: These columns were removed because they do not provide any predictive value for the model. They are identifiers and do not contribute to the success of the application.

### Compiling, Training, and Evaluating the Model

- **Neurons, Layers, and Activation Functions**:
  - **First Model**:
    - **First hidden layer**: 80 neurons, `relu` activation
    - **Second hidden layer**: 30 neurons, `relu` activation
    - **Output layer**: 1 neuron, `sigmoid` activation
  - **Second Model**:
    - **First hidden layer**: 85 neurons, `relu` activation
    - **Second hidden layer**: 30 neurons, `sigmoid` activation
    - **Output layer**: 1 neuron, `sigmoid` activation
  - **Third Model**:
    - **First hidden layer**: 100 neurons, `relu` activation
    - **Second hidden layer**: 50 neurons, `relu` activation
    - **Output layer**: 1 neuron, `sigmoid` activation

  These configurations were chosen based on experimentation with different numbers of neurons and activation functions to find the optimal model architecture. `ReLU` activation functions are commonly used for hidden layers to address the vanishing gradient problem, while `sigmoid` is used for the output layer in binary classification tasks to provide a probability score.

- **Model Performance**:
  - The target model performance aimed to achieve an accuracy of 75% on the test data. While the exact target accuracy was not always achieved, iterative tuning of the model hyperparameters (e.g., number of neurons, layers, activation functions) aimed to maximize this metric.

- **Steps to Increase Model Performance**:
  - **Data Scaling**: StandardScaler was used to normalize the feature data.
  - **Categorical Encoding**: One-hot encoding was applied to categorical variables to convert them into a numerical format suitable for training.
  - **Model Architecture Tuning**: Various configurations of neurons and layers were tested.
  - **Training Epochs**: The number of epochs was set to 100 to ensure sufficient training time for the model to learn from the data.
  - **Optimization Techniques**: Experimented with different optimization algorithms and learning rates.

### Summary

The deep learning model successfully predicted the success of charity donation applications, though achieving the exact target accuracy of 75% proved challenging. The model architecture, including the number of neurons, layers, and activation functions, was optimized through iterative experimentation.

**Recommendation**:
For further enhancement of model performance, consider the following approaches:
- **Ensemble Methods**: Combine multiple models (e.g., Random Forest, Gradient Boosting) to create an ensemble model that may capture more complex patterns in the data.
- **Hyperparameter Tuning**: Utilize grid search or randomized search to fine-tune hyperparameters systematically.
- **Feature Engineering**: Explore additional feature engineering techniques to create more informative features from the existing data.
- **Cross-Validation**: Implement cross-validation to ensure the model's performance is robust and generalizes well to unseen data.

By exploring these methods, it's possible to further improve the accuracy and reliability of the model in predicting the success of charity donation applications.

---

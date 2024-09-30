# deep-learning-challenge

# Alphabet Soup Neural Network Model Report

## Overview of the Analysis
The purpose of this analysis was to build a deep learning model that predicts the success of organizations funded by Alphabet Soup. Using historical data, the objective was to train a model that accurately identifies which organizations will effectively use their funding, thus helping Alphabet Soup make informed decisions. The target accuracy for the model was set to 75%.

---

## Results

### Data Preprocessing

- **Target Variable(s)**:
   - The target variable for the model was **`IS_SUCCESSFUL`**, which indicates whether the organization successfully used the funding.
   
- **Feature Variable(s)**:
   - The feature variables included:
     - `APPLICATION_TYPE`
     - `AFFILIATION`
     - `CLASSIFICATION`
     - `USE_CASE`
     - `ORGANIZATION`
     - `STATUS`
     - `INCOME_AMT`
     - `SPECIAL_CONSIDERATIONS`
     - `ASK_AMT`
   
- **Variables Removed**:
   - The following columns were removed as they did not contribute to the target prediction:
     - **`EIN`**: An identification column with no predictive value.
     - **`NAME`**: Another identification column with no predictive value.

### Compiling, Training, and Evaluating the Model

- **Neurons, Layers, and Activation Functions**:
   - The neural network model was designed with three hidden layers:
     - First hidden layer: **100 neurons** with the **`tanh`** activation function to handle both positive and negative inputs.
     - Second hidden layer: **100 neurons** with the **`relu`** activation function, chosen for its performance in deep learning tasks.
     - Third hidden layer: **100 neurons** with the **`relu`** activation function to add depth and increase the model's capacity.
   - **Dropout Layer**: A **30% dropout** was added after the third hidden layer to prevent overfitting.
   - **Output Layer**: The output layer used **1 neuron** with the **`sigmoid`** activation function, appropriate for binary classification.
   
- **Target Model Performance**:
   - The target accuracy was set at 75%, but the final model achieved an accuracy of **72.80%** with a loss of **0.5806**.
   
- **Steps to Increase Model Performance**:
   - Several optimization techniques were applied:
     - **Increased neurons** in all layers to 100 to give the model more capacity to learn complex patterns.
     - Added a **third hidden layer** to deepen the model.
     - Introduced a **dropout layer** to prevent overfitting.
     - Used the **Adam optimizer** with a **default learning rate** for optimization.

---

## Summary
The deep learning model was able to achieve a maximum accuracy of **72.80%**, which is below the target of 75%. Although the model performed reasonably well, it did not meet the desired accuracy threshold. Further optimization could potentially improve the results, but it may also indicate that a different type of model might be better suited for this task.

### Recommendation for Alternative Models:
- **Random Forest Classifier** or **Gradient Boosting**:
   - These models are generally more effective for classification tasks with tabular data and might outperform neural networks.
   - **Why**: Random forest and gradient boosting models can handle categorical data effectively and usually require less tuning compared to neural networks. They are robust and interpret data better when there are non-linear relationships in the dataset.
   - These models could potentially achieve higher accuracy with less complexity and are worth exploring as an alternative solution.

## Code Source
- Learning Assistant
- GitHub location: https://github.com/jeffjunohkim/deep-learning-challenge.git
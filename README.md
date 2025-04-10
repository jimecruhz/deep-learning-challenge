# Module 21 Report 

### **Alphabet Soup Deep Learning Model Report**
## Overview of the Analysis

* **Purpose of the analysis** - The purpose of this analysis was to develop a **binary classification model** that can predict whether applicants to **Alphabet Soup’s funding program** are likely to be **successful** or not. By using historical application data, we trained a deep learning neural network to identify patterns in key features and make accurate predictions.

The ultimate goal was to **reach at least 75% accuracy**, helping Alphabet Soup Foundation improve decision-making and funding efficiency.
## Results
* - **The Dataset** - 
	* -   **Target Variable**:
    
    -   `IS_SUCCESSFUL` (1 = success, 0 = not successful)
-   **Feature Variables**:
    
    -   All other columns after dropping non-beneficial fields (e.g., `EIN`, `NAME`, `STATUS`, `SPECIAL_CONSIDERATIONS`)
    -   Categorical variables (e.g., `APPLICATION_TYPE`, `AFFILIATION`, `CLASSIFICATION`) were one-hot encoded.
-   **Columns Removed**:
    
    -   `EIN`, `NAME`, `STATUS`, `SPECIAL_CONSIDERATIONS` — removed because:
        -   `EIN` and `NAME` are unique identifiers (not predictive)
        -   `STATUS` and `SPECIAL_CONSIDERATIONS` had low or single-value variability
        
*  **Compiling, Training, and Evaluating the Model**  - -   **Neural Network Architecture**:
    
    -   **Input Layer**: Number of input features (after encoding)
    -   **Hidden Layer 1**: 80 neurons, `relu` activation
    -   **Hidden Layer 2**: 30 neurons, `relu` activation
    -   **Output Layer**: 1 neuron, `sigmoid` activation (binary classification)
-   **Model Compilation Settings**:
    
    -   **Loss Function**: `binary_crossentropy`
    -   **Optimizer**: `adam`
    -   **Metrics**: `accuracy`
-   **Target Performance Achieved?**
    
    -   _Not quite_. The final model accuracy reached approximately **[insert your accuracy]**, just short of the 75% goal.
-   **Steps Taken to Improve Performance**:
    
    -   Added and removed hidden layers
    -   Adjusted the number of neurons in each layer
    -   Used different combinations of activation functions
    -   Tried feature engineering: binning values, removing low-variance features
    -   Normalized data with `StandardScaler`
    -   Ran additional training epochs (up to 100)
    

	




## Summary

While the model did not meet the target accuracy, it demonstrated reasonable performance and identified patterns in the data useful for prediction.

 I recommend trying Random Forest Classifier , Feature Selection, or Automated Hyperparameter

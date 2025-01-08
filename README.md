# Breast Cancer Detection using Neural Networks

This project demonstrates the implementation of a Neural Network model for breast cancer detection using TensorFlow and Keras. The model is trained on the Breast Cancer dataset from sklearn and achieves an accuracy of **96.49%** on the test data.

## Dataset
The Breast Cancer dataset is loaded from sklearn and includes 30 features. The dataset is split into training and testing sets, with the target variable indicating whether the tumor is malignant (`0`) or benign (`1`).

## Project Workflow

### 1. Data Collection & Preprocessing
- The data is loaded from sklearn's `load_breast_cancer` dataset.
- The data is converted into a pandas DataFrame for analysis.
- The target variable (`label`) is added to the DataFrame.
- The dataset is checked for missing values and basic statistical measures are computed.
- Features (`X`) and target (`Y`) are separated, and the dataset is split into training and testing sets.
- The features are standardized using `StandardScaler`.

### 2. Neural Network Model
- A Sequential Neural Network is built using TensorFlow and Keras with the following layers:
  - Flatten layer with input shape (30,).
  - Dense layer with 20 neurons and ReLU activation.
  - Dense output layer with 2 neurons and sigmoid activation.
- The model is compiled using:
  - Optimizer: Adam
  - Loss function: Sparse Categorical Crossentropy
  - Metric: Accuracy
- The model is trained for 10 epochs with a validation split of 10%.

### 3. Visualization of Accuracy and Loss
- Training and validation accuracy and loss are plotted to analyze the model's performance.

### 4. Model Evaluation
- The model achieves an accuracy of **96.49%** on the test data.

### 5. Predictive System
- A predictive system is implemented to classify a new tumor as malignant or benign based on the input data.

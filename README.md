# Credit Card Customer Churn Prediction

A Deep Learning project that predicts whether a bank customer is likely to leave the bank (customer churn prediction) using an Artificial Neural Network (ANN) built with TensorFlow and Keras.

---

## Project Overview

Customer churn prediction is an important problem in the banking sector. Banks lose revenue when customers stop using their services, so predicting churn early helps improve customer retention strategies.

In this project:

* Customer data is preprocessed using Pandas and Scikit-learn.
* Categorical variables are encoded.
* Features are standardized using `StandardScaler`.
* A Neural Network model is trained using TensorFlow/Keras.
* Model performance is evaluated using accuracy score.
* Training and validation graphs are visualized using Matplotlib.

---

## Technologies Used

* Python
* Pandas
* NumPy
* Scikit-learn
* TensorFlow / Keras
* Matplotlib
* Jupyter Notebook

---

## Dataset

The dataset used contains customer banking information such as:

* Credit Score
* Geography
* Gender
* Age
* Balance
* Number of Products
* Tenure
* Estimated Salary
* Active Membership Status
* Exited (Target Variable)

### Target Variable

* `Exited = 1` → Customer left the bank
* `Exited = 0` → Customer stayed

---

## Workflow

### 1. Data Preprocessing

* Loaded the dataset using Pandas
* Removed unnecessary columns:

  * `RowNumber`
  * `CustomerId`
  * `Surname`
* Applied One-Hot Encoding on:

  * `Geography`
  * `Gender`
* Split the dataset into training and testing sets
* Standardized the feature values

---

### 2. Model Architecture

The ANN model was built using Keras Sequential API.

#### Neural Network Structure:

| Layer          | Details                       |
| -------------- | ----------------------------- |
| Input Layer    | 11 Features                   |
| Hidden Layer 1 | 3 Neurons, Sigmoid Activation |
| Hidden Layer 2 | 2 Neurons, Sigmoid Activation |
| Output Layer   | 1 Neuron, Sigmoid Activation  |

---

### 3. Model Compilation

The model was compiled using:

* **Loss Function:** Binary Crossentropy
* **Optimizer:** Adam
* **Metric:** Accuracy

---

### 4. Model Training

* Trained for **100 epochs**
* Used validation split for monitoring performance

---

### 5. Evaluation

Predictions were made on the test dataset and converted into binary values using a threshold of `0.5`.

The model performance was evaluated using:

* Accuracy Score

---

## Visualizations

The project includes:

* Training Loss vs Validation Loss Graph
* Training Accuracy vs Validation Accuracy Graph

These plots help analyze:

* Model convergence
* Overfitting/Underfitting
* Training performance

---

## How to Run the Project

### 1. Clone the Repository

```bash
git clone <repository-link>
cd <repository-folder>
```

### 2. Install Dependencies

```bash
pip install numpy pandas matplotlib scikit-learn tensorflow
```

### 3. Run the Notebook

Open Jupyter Notebook and run:

```bash
jupyter notebook
```

Then open:

```bash
credit-card-customer-churn-project.ipynb
```

---

## Future Improvements

Some improvements that can be added:

* Hyperparameter tuning
* Using ReLU activation instead of Sigmoid in hidden layers
* Adding Dropout layers to reduce overfitting
* Trying advanced models like XGBoost
* Deploying the model using Flask or Streamlit

---

## Learning Outcomes

Through this project, concepts learned include:

* Data preprocessing
* Feature engineering
* Artificial Neural Networks (ANN)
* Binary classification
* Model evaluation
* Deep learning workflow using TensorFlow


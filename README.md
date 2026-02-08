# 🌊 Sonar Rock vs Mine Prediction System

## 📌 Project Overview
This project focuses on the binary classification of underwater objects using **Machine Learning**. By analyzing sonar signal patterns, the system determines whether an object is a **Rock (R)** or a **Naval Mine (M)**. This type of technology is essential for maritime safety and autonomous underwater vehicles.

## 🧠 Technical Architecture
- **Algorithm:** Logistic Regression (Binary Classification).
- **Optimization:** Used to find the best linear relationship between 60 sonar features and the target labels.
- **Platform:** Developed using Python in Google Colab.

## 🛠️ Tech Stack & Libraries
- **Language:** Python.
- **Pandas:** For data loading and statistical exploration.
- **NumPy:** For high-performance array manipulation.
- **Scikit-learn:** For data splitting (`train_test_split`), model training (`LogisticRegression`), and evaluation (`accuracy_score`).

## 📂 Dataset Details
- **Source:** Sonar dataset containing 208 observations.
- **Features:** 60 numerical columns representing the energy levels of sonar signals at different frequencies.
- **Labels:** One target column with 'R' (Rock) or 'M' (Mine).

## 📊 Detailed Workflow
- **Data Ingestion:** Load the sonar CSV file into a Pandas DataFrame for analysis.
- **Exploratory Data Analysis (EDA):** Perform `data.head()`, `data.shape()`, and `data.describe()` to understand data distribution.
- **Data Splitting:** Divide the dataset into **X** (Features) and **Y** (Target labels).
- **Training/Test Split:** Allocate 10% of the data for testing to ensure the model can handle unseen data.
- **Model Training:** Fit the Logistic Regression model to the training subset.
- **Evaluation:** Calculate the accuracy scores for both training and test phases.

## 📈 Performance Results
| Phase | Accuracy Score |
| :--- | :--- |
| Training Data | ~83% |
| Test Data | ~76% |

## 🔮 Predictive System Implementation
This system includes a functional script to process a single row of new data and output a human-readable prediction:

```python
import numpy as np

# Example of making a single prediction
input_data_reshaped = np.asarray(input_data).reshape(1, -1)
prediction = model.predict(input_data_reshaped)

if (prediction[0] == 'R'):
    print('Target: Rock')
else:
    print('Target: Mine')
```

## 🚀 How to Run

Follow these steps to set up and run the project on your local machine or in the cloud.

### 1. Prerequisite Setup
* Ensure you have **Python 3.8+** installed on your system.
* (Optional) It is recommended to use a virtual environment:
    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows: venv\Scripts\activate
    ```

### 2. Clone the Repository
```bash
git clone [https://github.com/krishkhatik01/Rock-VS-Mine-Model.git](https://github.com/krishkhatik01/Rock-VS-Mine-Model.git)
cd Rock-VS-Mine-Model

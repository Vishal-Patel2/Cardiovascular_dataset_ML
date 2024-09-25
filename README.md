# Cardiovascular Disease Detection Dataset

This repository contains a dataset for detecting cardiovascular diseases using machine learning techniques. It includes training, testing, and validation data, with corresponding labels and timing metrics that are crucial for model development.

## Dataset Files

### 1. `train_labels.csv`
- **Description**: Contains the training data labels for the patients.
- **Columns**:
  - `Patient_ID`: Unique identifier for each patient.
  - `Label`: Diagnosis label (0 = no cardiovascular disease, 1 = cardiovascular disease).

### 2. `test_labels.csv`
- **Description**: Contains the test data labels for model evaluation.
- **Columns**:
  - `Patient_ID`: Unique identifier for each patient.
  - `Label`: Diagnosis label (0 = no cardiovascular disease, 1 = cardiovascular disease).

### 3. `timing_test.xlsx`
- **Description**: Contains time-related metrics for the test set.
- **Columns**:
  - `Patient_ID`: Unique identifier for each patient.
  - `Timing_Metric`: Time-based data (e.g., symptom onset or test duration).

### 4. `timing_val.xlsx`
- **Description**: Contains time-related metrics for the validation set.
- **Columns**:
  - `Patient_ID`: Unique identifier for each patient.
  - `Timing_Metric`: Timing data relevant to cardiovascular health analysis.

## How to Use

1. **Training**: Use `train_labels.csv` to train your machine learning models. These labels are used for supervised learning.
2. **Testing**: Use `test_labels.csv` for model testing and performance evaluation.
3. **Timing Analysis**: Use the timing datasets (`timing_test.xlsx` and `timing_val.xlsx`) to incorporate time-based metrics in your model, which can improve the prediction of cardiovascular events.

## Data Format

- **CSV files**: Loadable using Python's **pandas** library.
- **Excel files**: Can be loaded using **pandas** (`read_excel()` function) or other Excel-compatible tools.

### Sample Code

```python
import pandas as pd

# Load CSV data
train_data = pd.read_csv('train_labels.csv')
test_data = pd.read_csv('test_labels.csv')

# Load Excel timing data
timing_test = pd.read_excel('timing_test.xlsx')
timing_val = pd.read_excel('timing_val.xlsx')

# Display the first few rows
print(train_data.head())
print(test_data.head())
print(timing_test.head())
print(timing_val.head())

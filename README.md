# **Machine Learning Approach - LSTM for Mining Process Quality Prediction**

## **Project Overview**
This project implements a Long Short-Term Memory (LSTM) model to predict the quality of silica concentrate in a mining process. The dataset contains information about various process variables, such as air flows, pulp levels, and chemical concentrations, which are used to predict the final product quality.

The project includes data preprocessing, feature engineering, hyperparameter tuning, and training of the LSTM model to achieve optimal prediction performance.
![image](https://github.com/user-attachments/assets/a5f6e500-7cac-4e05-8109-5f157ea084d2)

---

## **Dataset**
The dataset is sourced from Kaggle: [Quality Prediction in a Mining Process](https://www.kaggle.com/datasets/edumagalhaes/quality-prediction-in-a-mining-process/data).

### **Key Details of the Dataset**:
- **Source**: Kaggle
- **Data Description**: The dataset records hourly data from a flotation plant in a mining process, including:
  - Input variables like air flows, pulp pH, and chemical reagents.
  - Target variables: `% Silica Concentrate` and `% Iron Concentrate`.
- **File**: `MiningProcess_Flotation_Plant_Database.csv`
- **Total Records**: 737,453 rows
- **Columns**:
  - Process variables such as `% Iron Feed`, `% Silica Feed`, air flows, pulp density, and levels.
  - Target variable: `% Silica Concentrate`.

---

## **Project Workflow**

### 1. **Data Preprocessing**
   - **Handling Missing Values**: Resampled data to hourly intervals and addressed gaps in timestamps.
   - **Filtering**: Focused on data collected after a plant shutdown period for consistency.

### 2. **Feature Engineering**
   - **Feature Selection**: Selected features with strong correlations to the target variable while reducing multicollinearity.
   - **Interaction Features**: Created new features, such as `Air_pH_Interaction`, to capture important relationships.

### 3. **Model Development**
   - **LSTM Architecture**:
     - Deep LSTM with multiple layers.
     - Optimized using hyperparameters like learning rate, batch size, and the number of neurons.
   - **Hyperparameter Tuning**: Exhaustive grid search over a defined parameter grid to find the best configuration.
   - **Evaluation**:
     - Metrics: R² (0.65) score and MAE (0.1).
       
### 4. **Results**
   - Best model saved in `.h5` format.
   - Best hyperparameters and evaluation metrics saved for reproducibility.

---

## **How to Run the Project**

### 1. **Download repository**
```bash
git clone git@github.com:nicole-baltodano/Silica-concentrate-prediction.git
```

### 2. **Run the Jupyter notebook**
Run the `jupyter notebook`. Skip the fine-tunning part and directly load and test the model

### 3. **Results**
<p align="center">
    <img src="https://github.com/user-attachments/assets/ad0f81dc-77dc-4e70-8452-67c19507694f" alt="Image Description">
</p>

<p align="center">
    <img src="https://github.com/nicole-baltodano/nicole-baltodano.github.io/blob/main/images/time_series_silica.png" alt="Silica Time Series">
</p>

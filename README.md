# Credit-Card-Fraud-Detection
This project focuses on detecting fraudulent transactions using machine learning. Due to the imbalanced nature of fraud datasets, multiple resampling techniques such as **SMOTE**, **Random UnderSampling (RUS)**, and **Random OverSampling (ROS)** were applied to improve model performance.

---

##  **Overview**
- Explore the dataset and understand the class distribution.
- Preprocess the data, including feature scaling.
- Train and evaluate baseline models on the original imbalanced data.
- Apply resampling techniques to balance the data:
  - SMOTE (Synthetic Minority Over-sampling Technique)
  - Random UnderSampling (RUS)
  - Random OverSampling (ROS)
- Train classifiers on resampled data.
- Evaluate and compare model performance across different sampling methods.

---

##  **Tools & Libraries**
- **Python**
- **Pandas**, **NumPy**
- **Matplotlib**, **Seaborn**
- **Scikit-learn**
- **Imbalanced-learn** (SMOTE, RandomOverSampler, RandomUnderSampler)

---

##  **Dataset**
- **File**: `creditcard.csv`
- **Features**:
  - `Time`, `Amount` – Metadata
  - `V1` to `V28` – PCA-transformed features
  - `Class` – Target variable (0: Non-Fraud, 1: Fraud)
- **Challenge**: High imbalance with very few fraud cases compared to normal transactions

---

##  **Pipeline**

### 1. **Data Loading & Exploration**
- Load the dataset
- Check for nulls, datatypes, and summary statistics
- Explore the distribution of the target variable (`Class`)

### 2. **Visualization**
- Visualize class imbalance using bar charts
- Understand the proportion of fraudulent to non-fraudulent transactions

### 3. **Preprocessing**
- Split dataset into training and testing sets
- Scale `Time` and `Amount` using standardization

### 4. **Baseline Modeling**
- Train classifiers (Random Forest and Logistic Regression) on the original data
- Evaluate performance using accuracy, precision, recall, and F1-score

### 5. **Resampling Techniques**
- Apply Random UnderSampling to reduce the majority class
- Apply Random OverSampling to duplicate the minority class
- Apply SMOTE to synthetically generate new samples of the minority class

### 6. **Model Training on Resampled Data**
- Retrain classifiers on each resampled dataset
- Measure model effectiveness using key classification metrics

### 7. **Evaluation & Visualization**
- Collect evaluation metrics: Accuracy, Precision, Recall, F1-Score
- Visualize model performance comparison across all strategies using grouped bar charts

---

##  **Results**
- Performance comparison shows that models trained on resampled data (especially using SMOTE) perform significantly better in detecting fraud.
- SMOTE with Random Forest generally yields the best recall and F1-score.
- Balancing techniques are essential for high-performance fraud detection systems.

---

##  **Conclusion**
- Fraud detection datasets are typically imbalanced, which hurts the performance of standard classifiers.
- Resampling techniques like SMOTE, RUS, and ROS help improve model sensitivity to fraud.
- Random Forest consistently outperforms Logistic Regression.
- Visualizations help communicate model performance differences clearly and effectively.



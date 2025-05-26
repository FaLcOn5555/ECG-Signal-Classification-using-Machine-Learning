# 🩺 ECG Signal Classification using Machine Learning

I did this project using machine learning to classify ECG (Electrocardiogram) signals as **normal or abnormal** using real heartbeat data. It was inspired by the idea of using AI in predictive healthcare — helping detect irregular heart activity automatically using signal data.

---

## 📂 Dataset Used

The project uses ECG datasets from the **PTB Diagnostic ECG Database**. The files used are:
- `ptbdb_normal.xlsx` – contains normal ECG signals  
- `ptbdb_abnormal.xlsx` – contains abnormal ECG signals  

Each row in these files contains **187 numerical values** representing a patient's heartbeat signal.

---

##  Project Steps

### 1. 🧾 Data Loading
- Loaded the normal and abnormal ECG datasets using pandas
- Each sample was labeled:
  - `0` → normal
  - `1` → abnormal

### 2.  Preprocessing
- Added a `label` column to both datasets
- Combined both into a single DataFrame
- Shuffled the rows randomly for unbiased learning

### 3.  Splitting the Data
- Used `train_test_split()` to divide the data:
  - 80% for training  
  - 20% for testing

### 4.  Model Training
- Trained a **RandomForestClassifier** using the signal data  
- The model learned to detect patterns in ECG signals

### 5.  Model Evaluation
- The model achieved **100% accuracy** on the test set  
- Evaluated using:
  - Accuracy score
  - Confusion matrix
  - Precision, recall, and F1-score

---
## 📊 Results

The model's performance was **perfect**:

- ✅ Accuracy: **100%**
- ✅ Precision, Recall, F1-score: **All 1.00**

---

## 🖼️ Screenshots

### 📊 Normal vs Abnormal ECG Samples
![ECG Training Samples](screenshots/data_training.png)  
> Shows first 5 rows of normal and abnormal ECG data used for training.

### 📐 Merged Dataset Overview
![Dataset Shape](screenshots/dataset_shape.png)  
> Combined dataset with over 14,000 samples and 310 features.

### 📈 Final Model Evaluation
![Results Output](screenshots/result_data.png)  
> Model performance showing 100% accuracy and perfect classification report.

---

## 🛠️ Requirements

Install the dependencies using:
```bash
pip install -r requirements.txt

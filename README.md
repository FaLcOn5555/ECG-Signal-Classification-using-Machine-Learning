
# 🩺 ECG Signal Classification using Machine Learning

I did this project using machine learning to classify ECG (Electrocardiogram) signals as **normal** or **abnormal** using real heartbeat data. It was inspired by the idea of using AI in predictive healthcare — helping detect irregular heart activity automatically using signal data.

---

##  Dataset Used

The project uses ECG datasets from the **PTB Diagnostic ECG Database**. The files used are:
- `ptbdb_normal.xlsx` – contains normal ECG signals
- `ptbdb_abnormal.xlsx` – contains abnormal ECG signals

Each row in these files contains 187 numerical values representing a patient's heartbeat signal.

---

##  Project Steps

### 1. **Data Loading**
The normal and abnormal datasets were loaded using pandas and combined into one large dataset. Each sample was labeled:
- `0` for normal
- `1` for abnormal

### 2. **Preprocessing**
- Labeled both datasets with a `label` column
- Concatenated them into a single DataFrame
- Shuffled the rows randomly to ensure unbiased training

### 3. **Splitting the Data**
- Used `train_test_split()` to divide the dataset into:
  - **80% for training**
  - **20% for testing**

### 4. **Model Training**
- A **RandomForestClassifier** was trained using the ECG signal data.
- The classifier learned to distinguish between normal and abnormal patterns.

### 5. **Model Evaluation**
The model achieved **100% accuracy** on the test set (note: this might suggest a very clean or easy dataset).
- Accuracy score
- Confusion matrix
- Precision, recall, F1-score

### 6. **Saving the Model**
- Used `joblib` to save the trained model as `ecg_classifier_model.pkl`.

---

## 📊 Results

The model's performance was excellent:
- **Accuracy**: 100%
- **Precision/Recall/F1**: All perfect scores on both normal and abnormal classes

This shows strong potential for ECG classification using traditional machine learning.

---

##  Requirements

Install dependencies using:
```bash
pip install -r requirements.txt
```

---

##  How I ran the Project

1. Cloning the repository
2. Activating my virtual environment
3. Installing the requirements
4. Running the Jupyter notebook:
```bash
jupyter notebook
```
5. Open and execute `notebook.ipynb`

---

##  Acknowledgements

- PTB Diagnostic ECG Database (MIT-BIH / Physionet)
- scikit-learn team for Random Forest implementation

---

This project was built as a machine learning showcase for predictive diagnostics. It shows how classical ML models like Random Forest can be applied to biomedical signal classification, paving the way for more complex future models like CNNs or LSTMs for time series.


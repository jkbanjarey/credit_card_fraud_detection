# 💳 Credit Card Fraud Detection  

## 📌 Overview  
This project focuses on detecting fraudulent credit card transactions using **Machine Learning** techniques. Due to the **highly imbalanced nature** of fraud detection datasets, special techniques like **data balancing, anomaly detection, and advanced classification models** are implemented.  

## ✨ Features  
- 🔍 **Identifies fraudulent transactions with high accuracy.**  
- 📊 **Handles imbalanced datasets using techniques like SMOTE.**  
- 🤖 **Utilizes machine learning models such as Logistic Regression, Random Forest, and XGBoost.**  
- 📈 **Visualizes fraud patterns and feature correlations.**  

## 📂 Dataset  
The dataset used is **creditcard.csv**, which contains:  
- Dataset: https://media.geeksforgeeks.org/wp-content/uploads/20240904104950/creditcard.csv
- **Time & Amount** – Transaction time and amount.  
- **V1-V28** – Anonymized PCA-transformed features.  
- **Class** – Target variable (1 = Fraud, 0 = Non-Fraud).  

### 🔄 Data Preprocessing  
- **Checked for missing values and outliers.**  
- **Applied feature scaling (StandardScaler) for better model performance.**  
- **Handled imbalanced data using techniques like:**
  - Undersampling the majority class  
  - Oversampling using **SMOTE (Synthetic Minority Over-sampling Technique)**  

## 🛠 Requirements  
Install the required dependencies:  
```bash  
pip install numpy pandas matplotlib seaborn scikit-learn imbalanced-learn  
```  

## 🏗 Model Architecture  
The following models were tested:  
1. **Logistic Regression** – A baseline classifier.  
2. **Random Forest** – Handles imbalanced data well and captures feature importance.  
3. **XGBoost** – A gradient boosting approach for better fraud detection.  
4. **Neural Networks (Optional)** – For deep learning-based fraud classification.  

## 🏋️‍♂️ Training & Evaluation  
- **Split the dataset into train-test sets (80-20).**  
- **Trained models on balanced data.**  
- **Evaluated using Precision, Recall, F1-Score, and ROC-AUC.**  

## 📊 Insights & Results  
### 🔍 Key Insights:  
- **Only ~0.17% of transactions are fraudulent.**  
- **Fraud transactions have significantly lower amounts compared to normal transactions.**  
- **Class imbalance poses a challenge, requiring special handling.**  

### 📈 Results:  
| Model                | Precision | Recall | F1-Score | ROC-AUC |
|---------------------|-----------|--------|----------|----------|
| Logistic Regression | 92.3%     | 78.5%  | 84.7%    | 95.1%    |
| Random Forest      | 96.1%     | 81.2%  | 88.0%    | 97.5%    |
| XGBoost           | **98.2%**  | **85.6%** | **91.4%** | **98.8%** |

- **XGBoost performed the best**, achieving the highest accuracy and recall.  
- **Precision-Recall trade-off is crucial**, as high precision reduces false positives, while high recall ensures detecting actual fraud.  
- **Feature importance analysis** showed that some features significantly contribute to fraud detection.  

## 🚀 Usage  
To run the project, execute:  
```bash  
jupyter notebook credit_card_fraud.ipynb  
```  

## 🔮 Future Enhancements  
- 🏦 **Deploy as an API for real-time fraud detection.**  
- 🤖 **Implement deep learning (LSTMs, Autoencoders) for anomaly detection.**  
- 📡 **Use real-time streaming with Apache Kafka or Spark.**  

## 👨‍💻 Author  
**Jitendra Kumar Banjarey**  

## 📜 License  
This project is **open-source** and free for educational purposes. 🎓  

# Project-003-Spam-email-detector-logistic-regression-Naive-Bayes-

---
## 📖 Project Overview
This project implements a **spam email (SMS) detector** using **Machine Learning**.  
We trained two models — **Multinomial Naive Bayes** and **Logistic Regression** — to classify text messages as either:

- **Ham** → Legitimate/normal message  
- **Spam** → Unwanted/junk message (ads, scams, promotions, phishing, etc.)

---

## 📊 Dataset
- Source: [UCI SMS Spam Collection Dataset](https://archive.ics.uci.edu/ml/datasets/sms+spam+collection)  
- Total messages: **5572**  
  - **4825 ham (legit)**  
  - **747 spam (junk)**  

---

## 🔧 Project Workflow
1. **Data Loading** → Imported the SMS dataset into a Pandas DataFrame.  
2. **Data Preprocessing** →  
   - Converted all text to lowercase.  
   - Removed punctuation, numbers, and extra spaces.  
   - Prepared clean text for training.  
3. **Train-Test Split** →  
   - Training set: **4457 messages**  
   - Testing set: **1115 messages**  
4. **Feature Extraction** →  
   - Used **Bag of Words (CountVectorizer)** to convert text into numerical vectors.  
   - Each message represented by presence/absence of **6692 unique words**.  
5. **Model Training** →  
   - **Multinomial Naive Bayes**  
   - **Logistic Regression**  
6. **Model Evaluation** →  
   - Metrics: **Accuracy, Precision, Recall, F1-score**  
   - Confusion Matrix analysis  
7. **Prediction on Custom Messages** →  
   - Example:  
     - `"Congratulations! You won a free lottery ticket"` → **Spam**  
     - `"Hello, are we meeting tomorrow?"` → **Ham**

---

## 📈 Results

### 🔹 Multinomial Naive Bayes
- Accuracy: **96.7%**  
- Precision: **100%**  
- Recall: **75%**  
- F1-score: **86%**  

Confusion Matrix:
```

[[966   0]
[ 37 112]]

```

---

### 🔹 Logistic Regression
- Accuracy: **96.6%**  
- Precision: **100%**  
- Recall: **74%**  
- F1-score: **85%**  

Confusion Matrix:
```

[[966   0]
[ 38 111]]

```

---

## 📌 Key Insights
- Both models achieved **high accuracy (~96.6%)**.  
- **Precision = 100%** → The models never classify a ham message as spam (no false alarms).  
- **Recall ~ 75%** → Some spam messages are still misclassified as ham.  
- **Naive Bayes** is lightweight and slightly better in recall.  
- **Logistic Regression** is robust but had slightly lower recall.  

---

## 🚀 Future Improvements
- Use **TF-IDF Vectorizer** instead of simple Bag of Words.  
- Try **advanced ML models** (Random Forest, SVM).  
- Experiment with **deep learning (RNN/LSTM/Transformers)**.  
- Expand dataset with modern spam sources (emails, social media spam).  

---

## ✅ Conclusion
This project successfully built a **spam detector** capable of classifying SMS messages with over **96% accuracy**.  
It demonstrates how simple **NLP preprocessing + classical ML models** can produce powerful results in spam detection.  

---

# 🧠 Fake Review Detection & Product Category Classification

**Name:** Anushka Prajapati  
**Student ID:** 202301224  

This project applies **Natural Language Processing (NLP)** and **Machine Learning/Deep Learning** techniques to analyze e-commerce product reviews. It focuses on classifying product types and identifying fraudulent "fake" reviews.

---

## 📌 Project Overview
The objectives of this project are:
* **Product Category Classification:** Automatically identifying the category of a product based on user reviews.
* **Fake Review Detection:** Differentiating between genuine customer feedback and deceptive "opinionated" reviews.
* **Pattern Visualization:** Analyzing common linguistic traits of fake reviews using Word Clouds.

---

## 📂 Dataset Description
The dataset contains user reviews collected from an e-commerce platform.

| Column | Description |
| :--- | :--- |
| **category** | Product category |
| **rating** | Star rating (1–5) |
| **label** | Authenticity: **CG** (Genuine) or **OR** (Fake/Opinionated) |
| **text_** | Raw review text |

**Storage:** `data/processed/cleaned_reviews.csv`

---

## 🧪 Methodology

### 1️⃣ Data Preprocessing
* **Normalization:** Lowercasing, removing punctuation and numbers.
* **Tokenization:** Splitting text into individual tokens.
* **Stopword Removal:** Filtering out common filler words.
* **Lemmatization:** Reducing words to their root forms.

### 2️⃣ Feature Extraction
* **TF-IDF Vectorization:** Converting text into numerical vectors.
* **N-grams:** Using unigrams and bigrams for better context capture.

### 3️⃣ Model Implementations

#### **Machine Learning (Logistic Regression)**
* **Category Classification:** Multiclass model to predict product types.
* **Fake Review Detection:** Binary classification (Fake vs. Genuine).
* **Metrics:** Accuracy, Precision, Recall, and F1-score.

#### **Deep Learning (PyTorch LSTM)**
Implemented a **Long Short-Term Memory (LSTM)** network to capture sequential patterns in the text.



* **Architecture:** Embedding Layer → LSTM Layer → Fully Connected Output Layer → Sigmoid Activation.
* **Hardware:** Optimized for CPU training.

---

## 📊 Results Summary

| Task | Model | Performance |
| :--- | :--- | :--- |
| **Category Classification** | Logistic Regression | High Accuracy |
| **Fake Review Detection** | Logistic Regression | Strong Baseline |
| **Fake Review Detection** | LSTM (PyTorch) | Competitive |

### ☁️ Word Cloud Analysis
Generating a word cloud for **fake reviews (OR label)** highlighted:
* **Exaggerated Terms:** Frequent use of "book," "great," and "love."

---

## 📁 Project Structure
```text
Imitation_Fakespot_202301224/
│
├── data/
│   ├── raw/                 # Original dataset
│   └── processed/           # Cleaned data
│
├── notebooks/
│   ├── 01_eda.ipynb         # Exploratory Data Analysis
│   ├── 02_preprocess.ipynb  # Preprocessing Pipeline
│   ├── 03_vectorization.ipynb
│   ├── 04_pytorch_model.ipynb # LSTM model training
│   └── 05_wordcloud.ipynb   # Visualizations
│
├── src/
│   └── preprocessing.py     # Modular preprocessing script
│
├── requirements.txt         # Dependencies
└── README.md                # Project documentation

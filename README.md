# 📈 FinScan: High-Precision Financial News Sentiment Analyzer

FinScan is a specialized sentiment analysis pipeline designed to classify financial news headlines into **Bullish (Positive)** or **Bearish (Negative)** signals. While general-purpose NLP tools often struggle with financial context (e.g., labeling "market drop" as neutral), this project utilizes a custom-weighted financial lexicon to achieve a high-fidelity classification of **96.56% Accuracy**.

The model was trained and tested on a massive dataset of **1.4 million headlines**, ensuring robust performance across various market sectors and economic conditions.

---

## 🚀 Key Features

* **Custom Financial Lexicon:** Enhanced VADER engine with domain-specific weights (e.g., "lower", "surge", "crash") to fix context-blindness in standard tools.
* **Bigram TF-IDF Vectorization:** Utilizes 20,000 features including word pairs (NGrams) to capture relationships like "interest rate" or "stocks tumble".
* **Balanced Learning:** Implements `RandomUnderSampler` to ensure the model remains unbiased between positive and negative market signals.
* **Interactive Dashboard:** A built-in `ipywidgets` interface for real-time sentiment prediction and confidence scoring.

---

## 📊 Model Performance

The final model, a **Logistic Regression** classifier, significantly outperformed baseline Naive Bayes approaches after addressing label noise and class imbalance.

* **Accuracy:** 96.56%
* **Precision:** 94.87%
* **Recall (Sensitivity):** 98.44%
* **F1-Score:** 96.62%

### **Confusion Matrix**
The matrix demonstrates a remarkable ability to capture "Bullish" signals with very few false negatives.

---

## 🛠️ Tech Stack

* **Language:** Python 3.x
* **Data Handling:** Pandas, NumPy
* **NLP:** NLTK (VADER, WordNet Lemmatizer)
* **Machine Learning:** Scikit-Learn, Imbalanced-Learn
* **Visualization:** Matplotlib, Seaborn

---

## 💻 Installation & Usage

### **1. Clone the repository**
```bash
git clone [https://github.com/YOUR_USERNAME/FinScan-Sentiment-Analyzer.git](https://github.com/YOUR_USERNAME/FinScan-Sentiment-Analyzer.git)
pip install pandas scikit-learn nltk imbalanced-learn seaborn ipywidgets
```
# Data Set Link:
```
https://www.kaggle.com/datasets/abdullahbinshahbaz/analyst-ratings-processed-csv
```
# 📝 Analysis & Methodology
This project followed a rigorous Data Science lifecycle:

* **Preprocessing:** Lowercasing, regex-based special character removal, and stopword filtering (preserving directional words like "up/down").

* **Labeling Engine:** Developed a hybrid labeling function combining VADER compound scores with "Hard Rules" for critical financial terminology.

* **Vectorization:** Transformed cleaned text into numerical format using TfidfVectorizer with an ngram_range of (1, 2).

* **Evaluation:** Validated results using a 20% hold-out test set and cross-referencing with a manual sentiment check.
## Author: Abdullah-Bin-Shahbaz
Academic Institution: FAST School of Management, NUCES (Lahore Campus)


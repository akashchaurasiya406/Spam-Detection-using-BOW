# 📬 SMS Spam Detection System

A complete Natural Language Processing (NLP) and Machine Learning pipeline designed to classify SMS messages as either **spam** or **ham**[cite: 1]. This project uses **Bag of Words (BOW)** feature extraction combined with a **Multinomial Naive Bayes** classifier[cite: 1].

---

## 📂 Dataset Details
* **Source File:** `SMSSpamCollection.txt`[cite: 1]
* **Volume:** 5,572 rows of categorized text messages (Ham vs. Spam)[cite: 1].

---

## 🛠️ Tech Stack & Dependencies
To run and execute this project, the following standard Python libraries are required:
* **pandas & numpy** — For data manipulation and matrix operations[cite: 1].
* **nltk** — Natural Language Toolkit for stopwords and token filtering[cite: 1].
* **scikit-learn** — For feature extraction, model building, and evaluation metrics[cite: 1].
* **re** — Regular expressions for text preprocessing[cite: 1].

---

## ⚙️ Project Workflow

### 1. Data Cleaning & Preprocessing
* Removes non-alphabetic characters using regular expressions[cite: 1].
* Converts all words to lowercase for consistency[cite: 1].
* Tokenizes reviews and filters out standard English stopwords via NLTK[cite: 1].
* Applies `PorterStemmer` to reduce words to their root forms[cite: 1].

### 2. Feature Extraction (Bag of Words)
* Converts text corpus into numerical vectors using `CountVectorizer`[cite: 1].
* Constrained to a maximum feature size of **2,500**[cite: 1].
* Uses an n-gram range of `(1,2)` to account for both unigrams and bigrams[cite: 1].

### 3. Model Training & Splitting
* Encodes text labels into numerical/boolean arrays[cite: 1].
* Splits data into training and testing sets with an 80/20 train-test ratio[cite: 1].
* Instantiates and trains a `MultinomialNB` (Multinomial Naive Bayes) classifier model[cite: 1].

### 4. Evaluation & Performance
* Evaluates predictions using accuracy score and classification reports[cite: 1].
* **Accuracy Achieved:** ~98.11% on the test subset[cite: 1].
* High precision, recall, and F1-scores across both spam and ham classification classes[cite: 1].

# 🧠 MBTI Personality Type Predictor using NLP & XGBoost

This project is a machine learning application that predicts a user's MBTI (Myers-Briggs Type Indicator) personality type based on their written text. It uses Natural Language Processing (NLP) techniques and the XGBoost classifier for prediction.

---

## 📌 Features

- Predicts the MBTI personality type (e.g., INTJ, ENFP) from a block of text.
- Uses NLTK for text preprocessing:
  - Tokenization
  - Stopword removal
  - Stemming and lemmatization
- Converts text into numerical features using `CountVectorizer`.
- Trains four separate XGBoost classifiers for each MBTI trait:
  - Introversion (I) / Extroversion (E)
  - Intuition (N) / Sensing (S)
  - Thinking (T) / Feeling (F)
  - Judging (J) / Perceiving (P)
- Saves trained models and vectorizer using `pickle` for future predictions.

---

## 📁 Dataset

- **Source**: `mbti_1.csv`
- **Structure**:
  - `type`: MBTI type (e.g., INFP, ENTP)
  - `posts`: Collection of social media posts from the user

---

## ⚙️ Technologies Used

- Python
- Pandas, NumPy
- NLTK
- Scikit-learn
- XGBoost
- Pickle

---

## 🧪 How It Works

1. **Preprocessing**:
   - Clean and normalize user posts
   - Remove links, punctuation, and stopwords
   - Apply stemming and lemmatization

2. **Feature Extraction**:
   - Use `CountVectorizer` to convert cleaned text into numerical features

3. **Model Training**:
   - Train 4 separate `XGBClassifier` models (one for each MBTI trait)

4. **Prediction**:
   - A new input sentence is cleaned, vectorized, and passed through each model
   - The combined result gives the predicted MBTI type

---

## ▶️ Getting Started

### 1. Clone the repository

```bash
https://github.com/Shashivarunreddy/mbti-predictor.git
cd mbti-predictor


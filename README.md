# 📧 Spam Email Classification using Machine Learning

A machine learning project to classify emails as spam or not spam based on structured metadata. Developed as part of the B.Tech degree in CSE (AI) at KIET Group of Institutions, Ghaziabad.

## 📚 Overview

Spam emails are a major nuisance and a security concern. This project leverages metadata from a small dataset (`spam_emails.csv`) to build a spam classifier using a Random Forest model. The focus is on minimizing false positives while maintaining strong overall accuracy.

## 🧠 Problem Statement

Develop a model that classifies emails as **spam** or **not spam** using metadata features like:
- Number of links
- Number of attachments
- Sender reputation score

## 🎯 Objectives

- Clean and preprocess email metadata
- Train a Random Forest classifier
- Evaluate model performance with key metrics
- Visualize insights like feature importance and prediction probabilities

## 🗂 Dataset

- **File:** `spam_emails.csv`
- **Size:** 100 samples
- **Features:**
  - `num_links` (integer)
  - `num_attachments` (integer)
  - `sender_reputation` (float, range [0,1])
  - `is_spam` (yes/no)

## 🔧 Preprocessing

- Encoded `is_spam` to binary (1 = spam, 0 = not spam)
- Dropped rows with missing data
- Validated feature ranges for consistency

## 🛠️ Model Building

- **Algorithm:** Random Forest Classifier
- **Library:** `scikit-learn`
- **Train/Test Split:** 80/20
- **Random State:** 42
- **Features Used:** `num_links`, `num_attachments`, `sender_reputation`

## 📊 Evaluation Metrics

- **Accuracy**
- **Precision**
- **Recall**
- **F1-Score**
- **Confusion Matrix**

## 📈 Visualizations

- Confusion Matrix Heatmap (`confusion_matrix.png`)
- Feature Importance Plot (`feature_importance.png`)
- Probability Distribution Histogram (`predicted_probabilities.png`)

## ✅ Results Summary

- **Accuracy:** ~80%
- **Precision (Spam):** ~78%
- **Recall (Spam):** ~85%
- **F1-Score (Spam):** ~81%
- **Key Feature:** `sender_reputation`

## 🧠 Insights

- Most influential feature: `sender_reputation`
- Model handles false positives well (low disruption to legit emails)
- Small dataset is a limitation

## 🚀 Future Improvements

- Use a larger and more diverse dataset
- Add textual features (e.g., email subject or body content)
- Try more advanced models (e.g., XGBoost, LightGBM)
- Deploy as an API or integrate with email clients

## 📎 References

- [Scikit-learn Documentation](https://scikit-learn.org/stable/)
- [Seaborn Visualization](https://seaborn.pydata.org/)
- [UCI Spam Dataset](https://archive.ics.uci.edu/)

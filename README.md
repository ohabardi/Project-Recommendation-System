# 🧠 IBM Article Recommendation System

This project was developed as part of the Udacity Data Scientist Nanodegree program. It focuses on building a complete article recommendation system using real user interaction data from the IBM Watson Studio platform.

---

## 📌 Project Objectives

- Perform **Exploratory Data Analysis (EDA)** on user-article interactions.
- Build **Rank-Based Recommendations** for new users.
- Implement **User-User Collaborative Filtering** to personalize suggestions.
- Use **Natural Language Processing (NLP)** for **Content-Based Filtering** based on article titles.
- Train a **Matrix Factorization model (FunkSVD)** using the `surprise` library for advanced, latent-feature recommendations.

---

## 🧪 Methods Overview

| Method                      | Technique                     | Notes |
|----------------------------|-------------------------------|-------|
| Rank-Based Filtering       | Most popular articles         | Simple, cold-start safe |
| User-User Filtering        | Dot-product similarity        | Based on shared interactions |
| Content-Based Filtering    | TF-IDF + Cosine Similarity    | Built from article titles |
| Matrix Factorization (SVD) | FunkSVD from Surprise library | Most powerful, learns latent patterns |

---

## 📊 Data

- `user-item-interactions.csv`: Contains user IDs, article IDs, and titles
- The dataset tracks implicit feedback (views), not ratings

---

## 🧰 Tools & Libraries

- Python
- Pandas, NumPy, Scikit-learn
- `scikit-surprise` (SVD model)
- Google Colab (Jupyter Notebook environment)

---

## 📈 Example Output

```python
user_user_recs('0000b6...', m=5)
# [
#   "a beginner's guide to variational methods",
#   "data tidying in data science experience",
#   ...
# ]

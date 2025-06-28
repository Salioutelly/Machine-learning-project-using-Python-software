# Machine-learning-project-using-Python-software
# 📚 Book Rating Prediction Project

A machine learning regression project focused on predicting the average rating of books based on their metadata.

## 📌 Project Overview

Predicting the average rating of a book is tackled here as a **regression problem**, using **supervised machine learning** techniques. The goal is to estimate a continuous value (the rating) from a combination of features such as book title, authors, number of pages, reviews, language, and more.

---

## 🧱 Project Structure

The project is organized into five main steps:

1. **Data Exploration**
2. **Data Visualization**
3. **Feature Engineering**
4. **Modeling**
5. **Conclusion**

---

## 📊 1. Data Exploration

- **Dataset:** 11,123 rows and 12 columns  
- **No missing or duplicated values**

### 📈 Quantitative Features:
- `average_rating`: Mean rating received
- `num_pages`: Number of pages
- `ratings_count`: Number of ratings
- `text_reviews_count`: Number of text reviews

### 📝 Qualitative Features:
- `title`: Book title
- `authors`: One or more authors, separated by "/"
- `language_code`: Book language
- `publication_date`: Date of publication
- `publisher`: Publisher name

Additional identifiers: `bookID`, `isbn`, `isbn13`

---

## 📉 2. Data Visualization

Key visual insights include:

- **Distribution of average ratings** (KDE plot)
- **Top 10 books with the most text reviews**
- **Top 10 most prolific authors**
- **Authors with the highest total ratings count**
- **Correlation between average rating and other numeric variables**
- **Heatmap of feature correlations**  
  → Strong correlation (~87%) between `ratings_count` and `text_reviews_count`

---

## 🧪 3. Feature Engineering

- Outliers removed (e.g., books with more than 1500 pages)
- Additional variables engineered (e.g., `normalized_age`)
- Final selected features for modeling:
  - `num_pages`
  - `ratings_count`
  - `text_reviews_count`
  - `normalized_age`
  - `language`

---

## 🤖 4. Modeling

The dataset was split into:

- **80% training set**
- **20% test set**

Four models were trained and compared:

| Model            | Type             |
|------------------|------------------|
| Linear Regression| Baseline         |
| Decision Tree    | Tree-based       |
| Random Forest    | Ensemble         |
| XGBoost          | Gradient Boosted |

---

## ✅ 5. Conclusion

- **Random Forest** and **XGBoost** showed the best performance based on RMSE.
- These models are recommended for future deployment for their accuracy in predicting book ratings.

---

## 💻 Requirements

Install the following libraries before running the notebook:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn xgboost

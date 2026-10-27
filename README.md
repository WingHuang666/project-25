# project-25

# Dating App Reviews Analysis

## 1. Project Overview

This project analyzes user reviews from three dating applications: Tinder, Bumble, and Hinge. It uses Natural Language Processing (NLP), machine learning, Aspect-Based Sentiment Analysis (ABSA), and clustering techniques to explore user sentiment, review engagement, platform-specific language patterns, and common discussion topics.

The project combines supervised and unsupervised learning to examine user feedback from multiple perspectives.

## 2. Dataset

**Dataset:** `dating_app_reviews_sentiment.csv`

The dataset contains 10,709 user reviews from Tinder, Bumble, and Hinge.

Main variables include:

- `app_name`: Dating application name.
- `review_text`: Original user review.
- `rating`: User rating.
- `sentiment`: Positive or Negative sentiment label.
- `is_satisfied`: Binary satisfaction indicator.
- `thumbs_up`: Number of likes received by a review.
- `posted_at`: Review publication date.
- `review_word_count`: Number of words in the review.
- `review_char_len`: Number of characters in the review.

## 3. Research Questions

**RQ1 — Sentiment Prediction**

Can review text predict whether a user review expresses positive or negative sentiment?

**RQ2 — Review Engagement Prediction**

Can review content and related features predict whether a review receives at least one thumbs-up?

**RQ3 — Dating App Identification**

Can review text identify whether a review belongs to Tinder, Bumble, or Hinge?

**RQ4 — Sentiment Trends Over Time**

How does the proportion of negative reviews change over time across the three dating applications?

**RQ5 — Review Text Clustering**

Can reviews be grouped into meaningful clusters based on textual similarity, and how do these groups differ in sentiment, engagement, and platform composition?

## 4. Methodology

### Data Preprocessing and EDA

- Check missing values, duplicates, and variable types.
- Clean and normalize review text.
- Examine sentiment distributions, review lengths, and engagement patterns.
- Analyze monthly review activity and sentiment trends.

### Text Analysis

- TF-IDF vectorization using unigrams, bigrams, and trigrams.
- Multi-label aspect detection to identify multiple topics within individual reviews.
- Heuristic Aspect-Based Sentiment Analysis to examine sentiment toward specific aspects.

### Machine Learning Models

Classification models include:

- Logistic Regression
- Linear Support Vector Machine (SVM)
- Random Forest
- Dummy Classifier (baseline)

Models are compared using appropriate evaluation metrics, including Average Precision, F1-score, ROC-AUC, Accuracy, and Macro-F1.

Cross-validation is used for model selection, followed by held-out test evaluation. Feature importance is examined where supported by the selected models.

### Clustering

- TF-IDF text representation.
- Singular Value Decomposition (SVD) for dimensionality reduction.
- K-Means clustering.
- Elbow Method and Silhouette Score for cluster-number selection.
- Cluster profiling using keywords, sentiment, engagement, and app composition.

## 5. Tools and Libraries

**Language:** Python

**Main Libraries:**

- pandas and NumPy
- scikit-learn
- Matplotlib and Seaborn
- Quarto and Jupyter

## 6. Project Structure

```text
Dating-App-Reviews-Analysis/
├── dating_app_reviews_sentiment.csv
├── dating_app_review_project_FIXED.qmd
└── README.md
```

## 8. Notes

- Sentiment labels are associated with user ratings.
- Aspect detection and aspect-level sentiment analysis use heuristic rules and should be interpreted accordingly.
- Machine learning findings represent predictive associations rather than causal relationships.
- Clustering is exploratory, and cluster interpretations require careful validation.
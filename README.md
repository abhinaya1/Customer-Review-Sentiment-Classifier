# Customer Review Sentiment Classifier

## Project Overview

This project builds a **Natural Language Processing (NLP)** system to automatically classify customer reviews into **positive**, **neutral**, or **negative** sentiments.
The goal is to help businesses efficiently analyze large volumes of unstructured customer feedback and turn it into actionable insights.

This project was completed as part of the **Springboard Data Science Career Track Capstone**.


## Business Problem

Customer reviews contain valuable insights about product quality, delivery experience, and customer satisfaction. However:

* Reviews are **unstructured text**
* Manual analysis is **slow and inconsistent**
* Large review volumes make scaling difficult

An automated sentiment classification system enables faster, more consistent, and data driven decision making across teams.



## Data Science Problem Formulation

* **Task:** Supervised multi class classification
* **Input:** Customer review text
* **Output:** Sentiment label (Positive / Neutral / Negative)


## Dataset

* **Source:** Amazon US Customer Reviews Dataset (Kaggle)
* **Link:** [https://www.kaggle.com/datasets/cynthiarempel/amazon-us-customer-reviews-dataset](https://www.kaggle.com/datasets/cynthiarempel/amazon-us-customer-reviews-dataset)
* **Labeling Strategy:**

  * 1–2 stars → Negative
  * 3 stars → Neutral
  * 4–5 stars → Positive


##  Data Wrangling & Preprocessing

Key steps included:

* Removing missing and duplicate records
* Cleaning and normalizing review text
* Mapping star ratings to sentiment classes
* Tokenization and text vectorization using **TF-IDF**

**Key challenge:** Strong class imbalance toward positive reviews


##  Exploratory Data Analysis (EDA)

Key findings:

* Positive reviews dominate the dataset
* Neutral sentiment is underrepresented and harder to classify
* Negative reviews tend to be longer and more detailed
* Distinct vocabulary patterns exist across sentiment classes


##  Modeling Approach

### Feature Engineering

* **TF-IDF (Term Frequency–Inverse Document Frequency)** for text representation

### Models Evaluated

* Logistic Regression
* Linear Support Vector Machine (SVM)
* Naive Bayes (baseline)

### Evaluation Metrics

* Accuracy
* Precision, Recall
* **Macro F1 score** (emphasized due to class imbalance)


##  Results

* **Best performing models:** Logistic Regression & Linear SVM
* **Accuracy:** ~88%
* **Macro F1 score:** Met project success criteria (≥ 0.80)

Most classification errors occurred in the **neutral** class due to linguistic ambiguity.


##  Business Insights

* Negative sentiment often highlights delivery issues, product defects, and customer service problems
* Positive sentiment emphasizes value, reliability, and satisfaction
* Aggregated sentiment trends can reveal customer priorities at scale


## Recommendations

1. Deploy real time sentiment monitoring dashboards
2. Automatically route negative reviews to customer support teams
3. Use sentiment trends to inform product improvements and marketing strategies


##  Limitations & Future Work

**Limitations**

* Difficulty handling sarcasm and slang
* English only reviews
* Neutral sentiment remains challenging due to linguistic overlap

**Future Improvements**

* Fine tune transformer based models (e.g., BERT)
* Topic modeling on negative reviews
* Extend to multilingual sentiment analysis


##  Technologies Used

* Python
* pandas, NumPy
* scikit-learn
* NLTK / spaCy
* Matplotlib / Seaborn


##  Author

**Abhinaya Gyawali**
Springboard Data Science Career Track

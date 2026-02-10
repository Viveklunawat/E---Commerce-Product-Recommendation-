# Women's Clothing E-Commerce Analysis & Recommendation Prediction

##  Project Overview

This project analyzes **23,000+ customer reviews** from a women's clothing e-commerce platform to uncover **customer behavior, product performance issues, and business risks**, and to build a **machine learning model that predicts whether a customer will recommend a product**.

The project combines:

* Exploratory Data Analysis (EDA)
* Customer segmentation
* Product performance diagnostics
* NLP-based sentiment modeling

The final **Logistic Regression model achieved 88% accuracy**, with strong performance in identifying dissatisfied customers — a critical business objective.

---

##  Dataset Details

* **Total Records:** 23,483 reviews (23,480 after removing duplicates)
* **Target Variable:** `Recommend Flag` (0 = Not Recommended, 1 = Recommended)
* **Ratings:** 1–5 scale
* **Customer Age Range:** 18–99 years
* **Locations:** Mumbai, Bangalore, Gurgaon, Chennai
* **Sales Channels:** Web, Mobile

### Data Cleaning Steps

* Removed duplicate records
* Filled missing review titles and texts with empty strings
* Merged review title and review text into a single `review` column for NLP

---

##  Exploratory Data Analysis (EDA)

### Customer Demographics

* **Average customer age:** 43 years
* **Primary customer group:** 18–40 years (highest purchase volume)
* **Highest satisfaction:** Senior customers (60+) with **85.3% recommendation rate**

### Geographic Insights

* Customer behavior and satisfaction are **consistent across all cities**
* Gurgaon has the highest order volume
* Ratings remain stable (~4.2) across locations → strong national scalability

---

##  Product Performance Insights

### Category-Level Performance

* **General:** Most sold category
* **Intimates:** Least sold but **highest rated (4.29)**

### Subcategory1 Performance (Critical Finding ⚠️)

| Subcategory | Avg Rating | Insight              |
| ----------- | ---------- | -------------------- |
| Tops        | 4.17       | Best seller          |
| Dresses     | 4.15       | Strong performer     |
| Bottoms     | 4.29       | Highest satisfaction |
| **Trend**   | **3.82**   | ❌ Worst performing   |

🚨 **Trend subcategory is the only group with rating < 4.0 and lowest recommendation rate (73.9%) across all locations.**

---

## 📊 Recommendation Rate Summary

* **Overall Recommendation Rate:** 82.2%
* **Best Performing Subcategories:** Bottoms (85.1%), Intimates (85.0%)
* **Worst Performing:** Trend (73.9%)

This indicates a **systemic quality or product-market fit issue** in the Trend subcategory.

---

## 🧠 NLP & Sentiment Analysis

### Text Processing

* Cleaned using **spaCy** (lemmatization, stopword removal)
* TF-IDF vectorization used for feature extraction

### Word Cloud Insights

**Positive Reviews:**

* Fit, comfort, quality, fabric, flattering, perfect

**Negative Reviews:**

* Sizing issues, poor fabric quality, color mismatch, return problems

---

## 🤖 Machine Learning Models

### Objective

Predict whether a customer will **recommend a product** based on review text.

### Models Compared

| Model                   | Accuracy | Key Observation                    |
| ----------------------- | -------- | ---------------------------------- |
| Random Forest           | 85%      | Misses many dissatisfied customers |
| Multinomial NB          | 87%      | Poor recall for negative class     |
| **Logistic Regression** | **88%**  | Best balanced performance ✅        |

### Final Model: Logistic Regression

* **Accuracy:** 88%
* **Best recall & F1-score for non-recommended class**
* Most reliable for detecting dissatisfied customers early

---

## 🏆 Key Business Insights

1. **Trend Subcategory Crisis**

   * Lowest ratings, lowest sales, lowest recommendations
   * Requires immediate redesign or discontinuation

2. **Young Customers Drive Volume but Not Satisfaction**

   * Largest segment but lowest recommendation rate

3. **Senior Customers = High Loyalty Segment**

   * Small base, highest satisfaction → growth opportunity

4. **Web Dominates, Mobile Shows Higher Satisfaction**

   * Mobile UX improvements could increase conversions

---

## 🚀 Business Recommendations

**Immediate Actions**

* Audit Trend subcategory quality issues
* Deploy ML model for real-time dissatisfaction detection

**Short-Term**

* Improve sizing & quality consistency
* Target campaigns for Young customers

**Long-Term**

* Expand to new cities confidently
* Integrate ML feedback loop into product lifecycle

---

## 🧰 Tech Stack

* **Python**
* Pandas, NumPy
* Matplotlib, Seaborn
* spaCy (NLP)
* scikit-learn (ML)

---

## 📌 Key Takeaway

> The best business decisions are not driven by accuracy alone — they are driven by **risk, customer impact, and long-term trust**.

This project demonstrates how **data analysis + machine learning** can uncover hidden product risks and enable proactive decision-making in e-commerce.

---

⭐ *If you like this project, feel free to star the repository!*

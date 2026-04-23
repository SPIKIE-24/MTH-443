# 📊 Content Intelligence & Engagement Prediction System

## 🚀 Overview

This project builds a **multi-layer data mining system** to analyze social media posts and predict engagement.

It combines:

* Feature engineering
* PCA (dimension reduction)
* Clustering (unsupervised learning)
* Classification (supervised learning)
* Association analysis (rule mining)

---

## 📁 Repository Structure

```
project/
│
├── processed_data/        # Ready-to-use datasets
├── raw_data_sample/       # Small raw data subset
├── scripts/               # Full pipeline scripts
├── outputs/               # Plots & results
├── README.md
├── session_info.txt
```

---

## ⚡ Quick Start (IMPORTANT)

### 👉 Load ready dataset

```r
data <- readRDS("processed_data/final_with_pca_cluster.rds")
model_data <- readRDS("processed_data/model_data.rds")
```

👉 You DO NOT need to rerun preprocessing

---

## 🧠 What Has Already Been Done

### ✅ Data Pipeline

* Parsed raw post metadata
* Extracted hashtags and captions
* Merged influencer data

---

### ✅ Feature Engineering

* hashtag_count
* caption_length
* top 500 hashtag encoding

---

### ✅ PCA

* Reduced 500 features → 15 components
* Handled sparsity and noise

---

### ✅ Clustering

* K-means (k = 4)
* Found dominant + niche content groups

---

### ✅ Classification

* Logistic Regression → ~81% accuracy
* SVM → ~71% accuracy

---

### ✅ Association Analysis

* Manual Apriori-style implementation
* Extracted hashtag co-occurrence rules

---

## 🎯 Key Insights

* Content is not cleanly separable (weak clustering)
* Engagement is predictable (~81%)
* Hashtag combinations matter more than individual tags
* Linear models outperform nonlinear ones

---

## 🚀 What YOU Should Work On

### 🔥 1. Improve Models

* Random Forest / XGBoost
* Hyperparameter tuning
* Feature importance

---

### 🔥 2. NLP on Captions

* TF-IDF
* Word embeddings
* Language handling

---

### 🔥 3. Better Clustering

* Hierarchical clustering
* DBSCAN

---

### 🔥 4. Recommendation System

* Suggest best hashtags for a post
* Combine classification + association rules

---

### 🔥 5. Visualization

* PCA plots
* cluster visualization
* feature importance graphs

---

## ⚠️ Important Notes

* Do NOT redo preprocessing unless needed
* Use provided `.rds` files for speed
* Raw data is only for experimentation

---

## 🧠 Goal

Build a **smart recommendation system for content creators**

---

## 👥 Collaboration Notes

* Work modularly (one script per task)
* Keep code clean and documented
* Push updates regularly

---



## ▶️ How to Run the Project

1. Open R / RStudio

2. Set working directory to project folder

3. Run:

source("main_pipeline.R")

4. To skip preprocessing, directly load:

model_data <- readRDS("processed_data/model_data.rds")

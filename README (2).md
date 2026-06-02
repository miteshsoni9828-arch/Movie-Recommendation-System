# 🎬 Movie Recommendation System

<div align="center">

![Status](https://img.shields.io/badge/Status-Completed-success?style=for-the-badge)

<br/>

> **A Content-Based & Collaborative Filtering Movie Recommendation System built using a merged dataset of 45,000+ IMDB and 5,000+ TMDB records.**

</div>

---

## 📌 Project Overview

This project is a **Movie Recommendation System** that suggests movies to users based on their preferences. It combines two popular movie datasets — **IMDB** (45,000 records) and **TMDB** (5,000 records) — and applies machine learning techniques to deliver accurate and personalized recommendations.

The system analyzes movie features like genres, cast, crew, keywords, and overview to find similar movies and recommend them to the user.

---

## 🛠️ Tech Stack

| Tool / Library | Purpose |
|---------------|---------|
| `Python 3.8+` | Core programming language |
| `Pandas` | Data loading, merging, and cleaning |
| `NumPy` | Numerical operations |
| `Scikit-Learn` | TF-IDF Vectorizer, Cosine Similarity |
| `Matplotlib / Seaborn` | Data visualization and EDA |
| `NLTK` | Text preprocessing (stemming, stopwords) |
| `Jupyter Notebook` | Development environment |

---

## ⚙️ Project Workflow

```
📥 Load IMDB Dataset (45,000 records)
        +
📥 Load TMDB Dataset (5,000 records)
        ↓
🔗 Merge Datasets on Title / Year
        ↓
🧹 Data Cleaning & Preprocessing
   - Handle missing values
   - Remove duplicates
   - Normalize text fields
        ↓
🔍 Exploratory Data Analysis (EDA)
   - Genre distribution
   - Rating analysis
   - Most popular movies
        ↓
🧠 Feature Engineering
   - Combine: genres + keywords + cast + crew + overview
   - Text vectorization using TF-IDF
        ↓
📐 Cosine Similarity Calculation
        ↓
🎯 Recommendation Engine
        ↓
✅ Output: Top-N Similar Movie Recommendations
```

---

## 🔍 Key Features

- ✅ **Merged Dataset** — IMDB + TMDB combined for richer movie metadata
- ✅ **Content-Based Filtering** — Recommends movies based on movie features (genre, cast, keywords, overview)
- ✅ **TF-IDF Vectorization** — Converts text features into numerical vectors
- ✅ **Cosine Similarity** — Measures similarity between movies
- ✅ **EDA & Visualizations** — Genre distribution, ratings, popularity trends
- ✅ **Data Cleaning Pipeline** — Handles null values, duplicates, and inconsistent formats
- ✅ **Top-N Recommendations** — Returns top similar movies for any given input movie

---

## 📊 Exploratory Data Analysis (EDA)

The following EDA was performed on the merged dataset:

- 📈 **Genre Distribution** — Most common genres in the dataset
- ⭐ **Rating Analysis** — Distribution of IMDB and TMDB ratings
- 🗓️ **Year-wise Movie Count** — Movies released per year trend
- 🎭 **Top Cast & Crew** — Most frequent actors and directors
- 🔑 **Top Keywords** — Most used keywords across movies
- 🌍 **Language Distribution** — Movies by language

---

## 🧠 How Recommendation Works

1. **User inputs a movie name**
2. System finds the movie in the dataset
3. **TF-IDF vectorizer** converts the movie's combined features (genres + cast + keywords + overview) into a vector
4. **Cosine Similarity** is calculated between the input movie and all other movies
5. Top-N most similar movies are returned as recommendations

```python
# Example Usage
recommend("The Dark Knight")

# Output:
# 1. Batman Begins
# 2. The Dark Knight Rises
# 3. Inception
# 4. Interstellar
# 5. Man of Steel
```

---

## 📁 Project Structure

```
movie-recommendation-system/
│
├── data/
│   ├── imdb_movies.csv          # IMDB dataset (45,000 records)
│   ├── tmdb_movies.csv          # TMDB dataset (5,000 records)
│   └── merged_dataset.csv       # Final merged & cleaned dataset
│
├── notebooks/
│   ├── 01_data_merging.ipynb    # Dataset merging & cleaning
│   ├── 02_eda.ipynb             # Exploratory Data Analysis
│   └── 03_recommendation.ipynb  # Recommendation model
│
├── src/
│   ├── data_preprocessing.py    # Data cleaning functions
│   ├── feature_engineering.py   # Feature creation & vectorization
│   └── recommend.py             # Core recommendation logic
│
├── requirements.txt             # Python dependencies
└── README.md                    # Project documentation
```

---

## 📦 Requirements

```
pandas>=2.0.0
numpy>=1.24.0
scikit-learn>=1.3.0
matplotlib>=3.7.0
seaborn>=0.12.0
nltk>=3.8.0
jupyter>=1.0.0
```

Install all with:
```bash
pip install -r requirements.txt
```

---

## 📈 Results

- Successfully merged **45,000 IMDB + 5,000 TMDB** records into a unified dataset
- Built a content-based recommendation engine with **high similarity accuracy**
- System recommends **Top 10 similar movies** for any given movie input
- EDA revealed meaningful patterns in genres, ratings, and movie popularity trends

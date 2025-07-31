# 🎬 Movie Recommendation System using Machine Learning

This is a **Content-Based Movie Recommendation System** built using Python and machine learning techniques. It recommends movies based on similarity in plot keywords, cast, crew, and genres.

## 🚀 Project Overview

The system uses **Natural Language Processing (NLP)** and **cosine similarity** to recommend movies that are similar to a given input movie. It’s built using a dataset of over 4,800 movies sourced from Kaggle.

## 🛠️ Tech Stack

- **Python**
- **Pandas, NumPy**
- **Scikit-learn**
- **NLTK**
- **Jupyter Notebook**

---

## 🔧 Project Workflow

### 1️⃣ Data Collection
- Used Kaggle datasets: `movies.csv` and `credits.csv`
- Merged datasets on movie title

### 2️⃣ Data Preprocessing
- Dropped missing/null values
- Converted JSON-like columns using `ast.literal_eval()`
- Extracted features: `keywords`, `cast`, `crew`, `genres`
- Selected top 3 cast members and director

### 3️⃣ Feature Engineering
- Combined important text-based features into a single column: `tags`
- Cleaned text: removed spaces, lowercased, applied stemming using `PorterStemmer`

### 4️⃣ Vectorization
- Applied `CountVectorizer` with max features = 5000
- Removed stopwords for cleaner inputs

### 5️⃣ Similarity Computation
- Computed **cosine similarity** between all movie vectors
- Built a similarity matrix for fast lookup

### 6️⃣ Recommendation Logic
- A function that takes a movie name and returns top 5 similar movies

---

## 💡 Example

```python
recommend('Avatar')

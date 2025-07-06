# 🎧 Spotify Music Recommendation System with Clustering and NLP

This notebook implements a **Spotify music recommendation system** using both **clustering algorithms** and **Natural Language Processing (NLP)**. The goal is to recommend similar songs based on audio features or the combination of track and artist names.

---

## 🎼 Dataset

- Source: `spotify-2023.csv`
- Includes features like:
  - `track_name`, `artist(s)_name`, `streams`
  - Audio features: `bpm`, `danceability_%`, `valence_%`, `energy_%`, `acousticness_%`, `instrumentalness_%`, `liveness_%`, `speechiness_%`

---

## 🔍 Main Components

### 1. 🔧 Preprocessing
- Missing values replaced with `0`.
- Audio features scaled using `StandardScaler` and `MinMaxScaler`.

---

### 2. 🎯 Clustering-Based Recommendation
- Algorithm: **KMeans (5 clusters)**
- Songs are clustered by audio similarity.
- A **cosine similarity matrix** is calculated using normalized audio features.
- A function `recomendar_musicas` suggests the most similar songs based on a given track.

---

### 3. 🧠 NLP-Based Recommendation
- Combined `track_name` and `artist(s)_name` into a single string.
- Applied **TF-IDF vectorization** with English stopwords.
- Built a **cosine similarity matrix** from the TF-IDF vectors.
- A second recommendation function `recomendar_musicas_nlp` finds similar songs based on name and artist semantics.

---

## ✅ Results

Both recommendation systems return a list of 5 similar songs given an input track. They use:

- 🎵 **Clustering**: based on musical attributes (numerical similarity)
- 🧾 **NLP**: based on names and artist relationships (textual similarity)

---

## 📚 Libraries Used

- `pandas`, `matplotlib`, `seaborn`
- `sklearn`: KMeans, TF-IDF, cosine similarity, scalers
- `scipy` (indirectly via `cosine_similarity`)

---

## 💡 Possible Improvements

- Deploy with Streamlit for user interaction.
- Combine both systems into a hybrid model.
- Apply collaborative filtering based on user data (if available).

<!-- Achievement test -->

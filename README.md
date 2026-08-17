# 🎬 Movie Recommender System

A content-based movie recommendation web app built with Python and Streamlit. Enter any movie title and instantly get 5 personalized recommendations with posters fetched live from the TMDB API.

## 🚀 Live Demo
[https://moviesrecommender-jpm8k64u53svxyedcoqlup.streamlit.app/]

## 📌 Features
- Content-based filtering using cosine similarity
- Real-time movie poster fetching via TMDB REST API
- Interactive and responsive UI built with Streamlit
- Recommends 5 similar movies instantly from a dataset of 5,000+ titles

## 🛠️ Tech Stack
| Layer | Tools |
|---|---|
| Language | Python |
| ML / Data | Pandas, NumPy, Scikit-learn |
| Similarity Engine | Cosine Similarity (precomputed matrix) |
| API | TMDB API (The Movie Database) |
| Frontend | Streamlit |
| Serialization | Pickle |

## 🧠 How It Works

1. **Data Preprocessing** — Movie metadata (genres, cast, crew, keywords) is cleaned and combined into a single feature vector per movie
2. **Vectorization** — Text features are converted to numerical vectors using CountVectorizer
3. **Similarity Computation** — Cosine similarity is computed across all movie pairs and stored as a precomputed matrix
4. **Recommendation** — When a user selects a movie, the top 5 most similar movies are retrieved from the matrix
5. **Poster Fetching** — Movie IDs are used to call the TMDB API and fetch live poster images

## 📁 Project Structure
moviesrecommender/
│
├── app.py # Streamlit frontend + recommendation logic
├── main.py # Data preprocessing + similarity computation
├── movie recommender system.ipynb # EDA and model development notebook
├── movie_dict.pkl # Serialized movie dataframe
├── similarity.pkl # Precomputed cosine similarity matrix
├── requirements.txt # Dependencies
└── setup.sh # Streamlit config for deployment


## ⚙️ Installation & Setup
# 1. Clone the repository
git clone https://github.com/Krish-1710/moviesrecommender.git
cd moviesrecommender

# 2. Install dependencies
pip install -r requirements.txt

# 3. Run the app
streamlit run app.py

> **Note:** You'll need a TMDB API key. Get one free at [themoviedb.org](https://www.themoviedb.org/settings/api) and replace the key in `app.py`.

## 📊 Dataset
- Source: [TMDB 5000 Movie Dataset](https://www.kaggle.com/datasets/tmdb/tmdb-movie-metadata) (Kaggle)
- Size: 5,000+ movies with metadata including genres, cast, crew, and keywords

## 🔮 Future Improvements
- Add collaborative filtering for user-based recommendations
- Incorporate user ratings for hybrid recommendation
- Add search autocomplete and genre filters

## 👤 Author
**Krishkumar Patel**
- GitHub: [@Krish-1710](https://github.com/Krish-1710)
- LinkedIn: [krish-patel-213bab2a6](https://www.linkedin.com/in/krish-patel-213bab2a6/)

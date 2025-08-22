# 🎬 Movie Recommender System (TMDB Dataset)

A **content-based movie recommender system** built using **cosine similarity** on the TMDB dataset.  
This project suggests movies similar to a selected movie based on their content (genres, cast, crew, keywords, etc.), and displays their posters using the **TMDB API**.

---

## 🚀 Features
- ✅ Content-based recommendations using **cosine similarity**  
- ✅ Interactive **Streamlit web app**  
- ✅ Fetches real-time **movie posters** from TMDB API  
- ✅ Trained on the **TMDB 5000 Movies & Credits dataset**  
- ✅ Simple, fast, and user-friendly UI  

---

## 🗂️ Dataset
We used the **TMDB 5000 Movies Dataset**, which consists of:
- `tmdb_5000_movies.csv`
- `tmdb_5000_credits.csv`

The dataset contains information about:
- Movie titles  
- Genres  
- Keywords  
- Cast & Crew  
- Overview (plot description)  

📌 Source: [Kaggle - TMDB 5000 Movie Dataset](https://www.kaggle.com/datasets/tmdb/tmdb-movie-metadata)

---

## ⚙️ Tech Stack
- **Python 3**
- **Streamlit** (for UI)
- **Pandas, NumPy** (for data preprocessing)
- **Scikit-learn** (cosine similarity)
- **Pickle** (model storage)
- **Requests** (to fetch movie posters via TMDB API)

---

## 🏗️ How It Works
1. Preprocessing the dataset to extract important features (genres, cast, crew, keywords, overview).  
2. Combining these features into a single string per movie.  
3. Using **TF-IDF Vectorization** + **Cosine Similarity** to find similar movies.  
4. Storing the preprocessed data & similarity matrix in pickle files (`movie_list.pkl`, `similarity.pkl`).  
5. Deploying a **Streamlit app** (`app.py`) where users can:
	- Select a movie from the dropdown  
	- Get **Top 5 similar movies** with posters  

---

## ▶️ Usage

### 1️⃣ Clone the repository
```bash
git clone https://github.com/your-username/movie-recommender-system-tmdb-dataset.git
cd movie-recommender-system-tmdb-dataset
```

### 2️⃣ Install dependencies

```bash
pip install -r requirements.txt
```

### 3️⃣ Run the Streamlit app

```bash
streamlit run app.py
```

### 4️⃣ Select a movie & get recommendations 🎥🍿

---

## 📸 Demo

Example Recommendation for **Avatar**:

* Pirates of the Caribbean: At World's End
* Guardians of the Galaxy
* Star Trek
* John Carter
* Star Wars: Revenge of the Sith

(With posters displayed in the app)

---

## 📦 Project Structure

```bash
📂 movie-recommender-system-tmdb-dataset
 ┣ 📂 model
 ┃ ┣ movie_list.pkl
 ┃ ┗ similarity.pkl
 ┣ 📂 data
 ┃ ┣ tmdb_5000_movies.csv
 ┃ ┗ tmdb_5000_credits.csv
 ┣ app.py
 ┣ notebook.ipynb
 ┣ requirements.txt
 ┗ README.md
```

---

## 🔑 API Key Setup

This project uses the **TMDB API** for fetching posters.
Replace the API key in `app.py` with your own from [The Movie Database](https://www.themoviedb.org/settings/api).

```python
url = f"https://api.themoviedb.org/3/movie/{movie_id}?api_key=YOUR_API_KEY&language=en-US"
```

---

## 📌 Future Improvements

* 🎯 Add **hybrid recommendation** (content + collaborative filtering)
* 🔍 Implement **search functionality** for new movies
* 🌍 Deploy app on **Streamlit Cloud / Heroku**

---

## 👨‍💻 Author

**Kunal Chandra**

* 🔗 [GitHub](https://github.com/Kunalchandra007)
* 🔗 [LinkedIn](https://www.linkedin.com/in/kunal-chandra007)
* 🌐 [Portfolio](https://my-portfolio-zeta-ruby-26.vercel.app/)

---

✨ *If you like this project, give it a ⭐ on GitHub!*

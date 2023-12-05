# Movie Recommendation System with Streamlit README

## Introduction

This repository combines a Python script for a movie recommendation system with a Streamlit web application, providing a comprehensive solution. The movie recommendation system suggests 5 movies similar to a selected movie, while the Streamlit app offers a user-friendly interface for interactive exploration.

## Prerequisites

Before running the application or script, ensure you have the necessary libraries installed. You can install them using the following command:

```bash
pip install numpy pandas scikit-learn nltk streamlit
```

## Usage

1. Clone the repository:

   ```bash
   git clone https://github.com/your-username/movie-recommendation-web.git
   cd movie-recommendation-web
   ```

2. Download the dataset files (`tmdb_5000_movies.csv` and `tmdb_5000_credits.csv`) and place them in the same directory as the scripts.

3. Run the Streamlit web application:

   ```bash
   streamlit run app.py
   ```

   Replace `app.py` with the actual filename if different.

4. Open your web browser and navigate to the provided local host URL.

5. Choose a movie from the dropdown menu and click the "Recommend" button.

6. View the recommended movies displayed on the web page.

## Code Explanation

### Movie Recommendation System Script

The script (`recommend_movies.py`) preprocesses movie data, extracts features, and provides a function for recommending movies based on similarity.

```python
# def recommend(movie):
    movie_index = new_df[new_df['title'] == movie].index[0]
    distances = similarity[movie_index]
    movies_list = sorted(list(enumerate(distances)), reverse=True, key = lambda x:x[1])[1:6]
    for i in movies_list:
        print(new_df.iloc[i[0]].title)
```

### Streamlit Application

The Streamlit application (`app.py`) integrates the movie recommendation script and creates an interactive web interface, modifying the recommend(movie) function to be integrated with the UI.

```python
# def recommend(movie):
    movie_index = movies[movies['title'] == movie].index[0]
    distances = similarity[movie_index]
    movies_list = sorted(list(enumerate(distances)), reverse=True, key = lambda x:x[1])[1:6]
    recommended_movies = []
    for i in movies_list:
        movie_id = i[0]
        recommended_movies.append(movies.iloc[i[0]].title)
    return recommended_movies
```

### User Interface

The web interface allows users to select a movie from the dropdown menu and click a button to receive recommendations.

```python
# st.title("Movie Recommender System")
selected_movie_name = st.selectbox(
    'Choose Options: ',
    movies['title'].values
)

if st.button('Recommend'):
    recommendations = recommend(selected_movie_name)
    for i in recommendations:
        st.write(i)
```

## File Descriptions

- `app.py`: The Streamlit application script.
- `recommend_movies.py`: The main script for recommending movies.
- `tmdb_5000_movies.csv`: Dataset containing movie details.
- `tmdb_5000_credits.csv`: Dataset containing movie credits information.
- `movies.pkl`: Pickle file containing a dictionary of movie data.
- `similarity.pkl`: Pickle file containing the cosine similarity matrix.

## Note

- Ensure that the movie recommendation system script (`recommend_movies.py`) is in the same directory.
- The Streamlit application provides a simple and interactive way to explore movie recommendations.

Feel free to customize and enhance the web interface according to your preferences!

# Movie Recommender System with Streamlit README

## Introduction

This repository extends the movie recommendation system by integrating a user-friendly web interface using Streamlit. Users can interactively select a movie and receive recommendations through a simple web application.

## Prerequisites

Before running the application, make sure to install the required libraries. You can install them using the following command:

```bash
pip install streamlit pandas
```

## Usage

1. Clone the repository:

   ```bash
   git clone https://github.com/your-username/movie-recommender-web.git
   cd movie-recommender-web
   ```

2. Download the dataset files (`tmdb_5000_movies.csv` and `tmdb_5000_credits.csv`) and place them in the same directory as the script.

3. Run the Streamlit web application:

   ```bash
   streamlit run app.py
   ```

   Replace `app.py` with the actual filename if different.

4. Open your web browser and navigate to the provided local host URL.

5. Choose a movie from the dropdown menu and click the "Recommend" button.

6. View the recommended movies displayed on the web page.

## Code Explanation

### Streamlit Application

The Streamlit application (`app.py`) utilizes the `recommend` function from the movie recommendation script and creates an interactive web interface.

```python
# Streamlit Application
# ...
```

### User Interface

The web interface allows users to select a movie from the dropdown menu and click a button to receive recommendations.

```python
# User Interface
# ...
```

## File Descriptions

- `app.py`: The Streamlit application script.
- `recommend_movies.py`: The main script for recommending movies (as discussed in the previous README).
- `tmdb_5000_movies.csv`: Dataset containing movie details.
- `tmdb_5000_credits.csv`: Dataset containing movie credits information.
- `movies.pkl`: Pickle file containing a dictionary of movie data.
- `similarity.pkl`: Pickle file containing the cosine similarity matrix.

## Note

- Ensure that the movie recommendation system script (`recommend_movies.py`) is in the same directory.
- The Streamlit application provides a simple and interactive way to explore movie recommendations.

Feel free to customize and enhance the web interface according to your preferences!

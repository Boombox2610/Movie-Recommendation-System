# Movie Recommendation System README

## Introduction

This repository contains a Python script for a movie recommendation system. The system recommends 5 movies similar to a selected movie based on various features such as overview, genres, keywords, cast, and crew.

## Prerequisites

Before running the script, ensure you have the necessary libraries installed. You can install them using the following command:

```bash
pip install numpy pandas scikit-learn nltk
```

## Usage

1. Clone the repository:

   ```bash
   git clone https://github.com/your-username/movie-recommendation-system.git
   cd movie-recommendation-system
   ```

2. Download the dataset files (`tmdb_5000_movies.csv` and `tmdb_5000_credits.csv`) and place them in the same directory as the script.

3. Run the script:

   ```bash
   python recommend_movies.py
   ```

   Replace `recommend_movies.py` with the actual filename if different.

4. Enter the title of the movie when prompted.

5. The script will output the top 5 recommended movies based on similarity.

## Code Explanation

### Data Preprocessing

The script preprocesses the movie data by cleaning and transforming features such as genres, keywords, cast, and crew.

```python
# Data Preprocessing
# ...
```

### Feature Extraction

The script uses natural language processing techniques to extract features from the movie data.

```python
# Feature Extraction
# ...
```

### Recommendation Function

The `recommend` function takes a movie title as input and outputs 5 recommended movies.

```python
# Movie Recommendation Function
# ...
```

## File Descriptions

- `recommend_movies.py`: The main script for recommending movies.
- `tmdb_5000_movies.csv`: Dataset containing movie details.
- `tmdb_5000_credits.csv`: Dataset containing movie credits information.
- `movies.pkl`: Pickle file containing a dictionary of movie data.
- `similarity.pkl`: (Currently commented out) Pickle file containing the cosine similarity matrix.

## Note

- The script uses the CountVectorizer and cosine similarity from scikit-learn for feature extraction and similarity computation.
- The output of the recommendation is displayed in the console.

Feel free to explore and modify the script to suit your needs!

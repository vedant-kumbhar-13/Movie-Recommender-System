##  Movie Recommendation System

This project is a content-based movie recommender system built with Python. It uses a dataset of 5000 movies from TMDb to suggest movies with similar content (plot, cast, director, genres).

The core logic is built in the Jupyter Notebook (recommender system.ipynb). It involves:

Loading and merging two datasets (movies and credits).

Cleaning and preprocessing text data (overview, genres, keywords, cast, crew).

Creating a unified "tags" column for each movie.

Applying text vectorization (CountVectorizer) and stemming (NLTK).

Calculating the similarity between all movies using Cosine Similarity.

Saving the final processed data (movie_list.pkl) and the similarity matrix (similarity.pkl) for use in a web app.

##  Technologies Used

Python

Jupyter Notebook

Pandas

NumPy

NLTK (for stemming)

Scikit-learn (for CountVectorizer and cosine_similarity)

## How to Run This Project

Clone this repository:

git clone [https://github.com/your-username/Movie-Recommendation-System.git](https://github.com/your-username/Movie-Recommendation-System.git)


Create a folder named data in the project directory.

Download the "TMDB 5000 Movie Dataset" from Kaggle:
https://www.kaggle.com/datasets/tmdb/tmdb-movie-metadata

Place the tmdb_5000_movies.csv and tmdb_5000_credits.csv files inside the data/ folder.

Install the required libraries:

pip install -r requirements.txt


Run the recommender system.ipynb notebook. It will read from the data/ folder and generate the final model files in the artificats/ folder.

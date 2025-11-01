## Movie Recommendation System & Web App

This project consists of two main components:

A content-based movie recommendation model built in a Jupyter Notebook.

A fully functional web application built with Streamlit that serves the model's recommendations.

The recommendation model uses a dataset of 5000 movies from TMDb to suggest movies with similar content (plot, cast, director, genres).

## Core Logic (Jupyter Notebook)

Data Processing: Loaded and merged two datasets (movies and credits).

Feature Engineering: Cleaned and preprocessed text data (overview, genres, keywords, cast, crew) to create a unified "tags" column.

Vectorization: Applied CountVectorizer and NLTK stemming to convert text tags into a numerical vector space.

Modeling: Calculated the cosine_similarity between all movies to find the most similar items.

Export: Saved the processed data (movie_list.pkl) and the similarity matrix (similarity.pkl) for the web app.

## Web Application (Streamlit)

The app.py file uses Streamlit to create an interactive user interface. It loads the saved .pkl files, takes a movie title as input from the user, and instantly returns the top 5 most similar movies.

## Technologies Used

Model: Python, Pandas, NumPy, NLTK, Scikit-learn, Jupyter Notebook

Web App: Streamlit

## Deployment: Procfile and setup.sh for deployment on platforms like Streamlit Cloud.

## How to Run This Project

There are two ways to run this project:

## Option 1: Run the Streamlit Web App (Recommended)

This will run the pre-trained model in an interactive web app.

Clone this repository:

git clone [https://github.com/vedant-kumbhar-13/Movie-Recommender-System.git](https://github.com/vedant-kumbhar-13/Movie-Recommender-System.git)
cd Movie-Recommender-System


Install the required libraries:

pip install -r requirements.txt


Run the Streamlit app:

streamlit run app.py


Your browser will automatically open with the app.

## Option 2: Re-train the Model from Scratch

This will re-run the Jupyter Notebook to re-generate the .pkl model files.

Create a folder named data in the project directory.

Download the "TMDB 5000 Movie Dataset" from Kaggle:
https://www.kaggle.com/datasets/tmdb/tmdb-movie-metadata

Place the tmdb_5000_movies.csv and tmdb_5000_credits.csv files inside the data/ folder.

Run the recommender system.ipynb notebook. It will generate the final model files in the root directory.

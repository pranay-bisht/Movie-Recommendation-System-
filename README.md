# Movie-Recommendation-System
A content-based movie recommendation system using TF-IDF and cosine similarity to suggest similar movies based on genres, keywords, tagline, cast, and director.

This project implements a content-based movie recommendation system using TF-IDF vectorization and cosine similarity to recommend movies based on various features such as genres, keywords, tagline, cast, and director.

Table of Contents
Overview
Features
Technologies Used
How It Works
Setup and Installation
Usage
Future Improvements
Contributing
License
Overview
The goal of this project is to recommend movies to users based on the similarity of movies' content. The system analyzes movie features (like genres, keywords, cast, etc.) and calculates the similarity between the movies using cosine similarity. Given a user's favorite movie, the system suggests movies that are closely related to it.

Features
Content-Based Recommendations: Recommends movies based on movie features.
Customizable Input: Users can input any movie title, and the system will provide similar movies.
Multiple Features: The recommendation is based on a combination of genres, keywords, tagline, cast, and director.
Technologies Used
Python: Programming language used to build the recommendation engine.
Pandas: Used for data manipulation and loading the dataset.
Scikit-learn: For vectorizing text data using TfidfVectorizer and calculating cosine similarity.
Difflib: Used to find close matches for the movie names entered by the user.
How It Works
Data Preprocessing:

The dataset contains multiple features such as genres, keywords, tagline, cast, and director.
These features are combined into a single string for each movie.
TF-IDF Vectorization:

The combined features are converted into a matrix of TF-IDF features.
TF-IDF (Term Frequency-Inverse Document Frequency) helps in determining the importance of a word in a document relative to a collection of documents.
Cosine Similarity Calculation:

The cosine similarity between the TF-IDF vectors of the movies is calculated.
Cosine similarity measures the cosine of the angle between two vectors, providing a similarity score between 0 and 1.
Movie Recommendation:

Based on the user's favorite movie input, the system finds the most similar movies and returns a list of recommended movies.

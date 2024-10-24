# Movie Recommendation System Using Cosine Similarity

This project implements a **content-based movie recommendation system** using **TF-IDF vectorization** and **cosine similarity** to recommend movies based on various features such as genres, keywords, tagline, cast, and director.

## Table of Contents
- [Overview](#overview)
- [Features](#features)
- [Technologies Used](#technologies-used)
- [How It Works](#how-it-works)
- [Setup and Installation](#setup-and-installation)
- [Usage](#usage)
- [Future Improvements](#future-improvements)
- [Contributing](#contributing)
- [License](#license)

## Overview
The goal of this project is to recommend movies to users based on the similarity of movies' content. The system analyzes movie features (like genres, keywords, cast, etc.) and calculates the similarity between the movies using cosine similarity. Given a user's favorite movie, the system suggests movies that are closely related to it.

## Features
- **Content-Based Recommendations**: Recommends movies based on movie features.
- **Customizable Input**: Users can input any movie title, and the system will provide similar movies.
- **Multiple Features**: The recommendation is based on a combination of genres, keywords, tagline, cast, and director.

## Technologies Used
- **Python**: Programming language used to build the recommendation engine.
- **Pandas**: Used for data manipulation and loading the dataset.
- **Scikit-learn**: For vectorizing text data using `TfidfVectorizer` and calculating cosine similarity.
- **Difflib**: Used to find close matches for the movie names entered by the user.

## How It Works

### Data Preprocessing:
- The dataset contains multiple features such as genres, keywords, tagline, cast, and director.
- These features are combined into a single string for each movie.

### TF-IDF Vectorization:
- The combined features are converted into a matrix of TF-IDF features.
- TF-IDF (Term Frequency-Inverse Document Frequency) helps in determining the importance of a word in a document relative to a collection of documents.

### Cosine Similarity Calculation:
- The cosine similarity between the TF-IDF vectors of the movies is calculated.
- Cosine similarity measures the cosine of the angle between two vectors, providing a similarity score between 0 and 1.

### Movie Recommendation:
- Based on the user's favorite movie input, the system finds the most similar movies and returns a list of recommended movies.

## Setup and Installation
1. Clone the repository:
    ```bash
    git clone https://github.com/your-username/movie-recommendation-system.git
    ```

2. Navigate to the project directory:
    ```bash
    cd movie-recommendation-system
    ```

3. Install the required dependencies:
    ```bash
    pip install -r requirements.txt
    ```

4. Place your dataset (`movies.csv`) in the project directory. The dataset should contain the following columns:
    - `index`: Unique identifier for each movie
    - `title`: Movie title
    - `genres`, `keywords`, `tagline`, `cast`, `director`: Features used for recommendation

5. Run the script:
    ```bash
    python movie_recommender.py
    ```

## Usage
1. After running the script, you will be prompted to enter your favorite movie name:
    ```bash
    Enter your favourite movie name: batman
    ```

2. The system will then find similar movies based on the input and display a list of recommendations:
    ```bash
    Movies suggested for you:
    1. Batman Begins
    2. The Dark Knight
    3. Batman Returns
    4. ...
    ```

## Future Improvements
- **Incorporate User Feedback**: Collect user feedback on recommendations to refine the system over time.
- **Hybrid Recommender System**: Combine content-based and collaborative filtering methods for more personalized recommendations.
- **Expand Feature Set**: Add more movie attributes (e.g., reviews, ratings) to improve recommendation accuracy.

## Contributing
Contributions are welcome! If you want to contribute, please fork the repository, create a new branch, and submit a pull request with your changes.

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

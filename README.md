# Capstone 8 – Recommendation System

## Project Overview

This project builds a simple **content-based movie recommendation system** using the MovieLens dataset.

The goal is to recommend movies that are similar to a movie selected by the user. The system uses movie **genres and user-generated tags** as content features and calculates similarity between movies using **cosine similarity**.

The project was developed as part of the **Machine Learning Models – Capstone 8** project.

---

## Dataset

The project uses the **MovieLens Latest Small Dataset**.

The dataset contains information about:

* Movies
* Movie genres
* User ratings
* User-generated tags
* Movie links/identifiers

The main files used are:

* `movies.csv`
* `ratings.csv`
* `tags.csv`
* `links.csv`

The raw dataset is stored in:

`Data/Raw/`

---

## Project Objectives

The main objectives of this project are to:

1. Load and explore the MovieLens dataset.
2. Analyze movie genres and tags.
3. Create numerical features from movie genres and tags.
4. Combine the content features into one feature matrix.
5. Calculate movie-to-movie similarity using cosine similarity.
6. Build a recommendation function.
7. Generate recommendations for selected movies.
8. Evaluate the recommendation results.
9. Save processed data and final visualizations.

---

## Recommendation Approach

This project uses **content-based filtering**.

The recommendation system compares movies based on their available content information rather than relying only on ratings from other users.

### Features Used

Two main types of content features were used:

### 1. Movie Genres

Movie genres were converted into numerical features using one-hot encoding.

Examples include:

* Action
* Adventure
* Animation
* Comedy
* Crime
* Drama
* Fantasy
* Horror
* Romance
* Sci-Fi
* Thriller
* and other genres

### 2. Movie Tags

User-generated movie tags were also converted into numerical features.

The genre and tag features were combined to create the final movie feature matrix.

The processed feature file is saved as:

`Data/Processed/movie_features.csv`

---

## Cosine Similarity

The recommendation system uses **cosine similarity** to measure how similar two movies are based on their content features.

A similarity score closer to **1** indicates that two movies have more similar feature profiles.

The system calculates a similarity matrix between the movies and uses the similarity scores to identify the most similar movies.

---

## Example Recommendation

One of the test movies used in the project was:

**Toy Story (1995)**

The system generates a ranked list of movies based on their similarity to the selected movie.

The final Toy Story recommendation results are saved in:

`Data/Final/toy_story_recommendations.csv`

A visualization of the recommendations is also saved as:

`Data/Final/toy_story_recommendations.png`

---

## Additional Analysis

The project also includes an analysis of movie genres.

The top 10 movie genres are visualized in:

`Data/Final/top_10_movie_genre.png`

These visualizations help demonstrate the distribution of movie genres and the recommendation results.

---

## Model Testing and Evaluation

The recommendation function was tested using multiple movies, including:

* Toy Story (1995)
* Matrix, The (1999)
* Jumanji (1995)

The evaluation checked that:

* The requested number of recommendations was returned.
* The original movie was not included in its own recommendations.
* Similarity scores were valid.
* Recommendations were sorted by similarity score.

The recommendation system successfully passed these checks.

---

## Project Structure

```text
Capstone-8-Recommendation-System/
│
├── Data/
│   ├── Raw/
│   │   ├── movies.csv
│   │   ├── ratings.csv
│   │   ├── tags.csv
│   │   ├── links.csv
│   │   └── README.txt
│   │
│   ├── Processed/
│   │   └── movie_features_
```

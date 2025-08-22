# Book-Recommendation-Project
Portfolio-Project-Ironhack


## Project Overview
This project implements a **Book Recommendation Engine** using Python. It demonstrates how to design, develop, and evaluate a recommendation system using both **content-based** and **cluster-based** methods. By the end, users can input a book and receive personalized recommendations based on similarity in features or metadata.

---

## Features

1. **Data Cleaning & Preprocessing**  
   - Handles missing and duplicate values in numeric and categorical features.
   - Scales numeric features for clustering algorithms.

2. **Cluster-Based Recommendations**  
   - Uses K-Means clustering on numeric features (`Page_Count`, `Avg_Rating`, `Num_Ratings`).
   - Returns top N books from the same cluster as the input book.

3. **Content-Based Recommendations**  
   - Combines textual metadata (`Author`, `Categories`, `Publisher`).
   - Uses **TF-IDF vectorization** and **cosine similarity** to find the most similar books.
   - Returns the top 5 books that are most similar in content.

4. **Visualization**  
   - Scatter plots for cluster visualization (`Avg_Rating` vs `Num_Ratings`).
   - Bar plots for top categorical values like `Author`, `Publisher`, `Categories`.
   - Optional: save plots as images for reporting.

---

## Data Sources

- **Scraping websites** (ensure compliance with robots.txt):
  - [Goodreads](https://www.goodreads.com/) – titles, authors, genres, ratings, reviews.
  

- **APIs**:
  - [Google Books API](https://developers.google.com/books/docs/v1/using)

## Dependencies include:

- pandas
- numpy
- scikit-learn
- matplotlib
- seaborn
- Jupyter Notebook or JupyterLab

## Evaluation

- Cluster-Based Method: Use silhouette score to evaluate clustering quality.
- Content-Based Method: Check recommendations for relevance based on book metadata.
- Compare results to find which approach provides the most meaningful recommendations.


## Project Goals

- Apply data science techniques to a real-world recommendation problem.
- Gain hands-on experience with clustering, TF-IDF, and cosine similarity.
- Build a functional prototype that generates personalized book recommendations.


import pandas as pd
df = pd.read_csv("books.csv")

from recommender import recommend_similar_items
recommendations = recommend_similar_items(item_index=10, df=df, n_recommendations=5)
print(recommendations)

from recommender import get_recommendations
recommendations = get_recommendations('1984', df=df)
print(recommendations)


## Link 

## Contact

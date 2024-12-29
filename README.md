# 📚 Book Recommendation System

A hybrid book recommendation system that combines **content-based filtering** and **collaborative filtering** to suggest books based on user preferences, ratings, and book metadata.

## 🎯 Project Overview

This project aims to develop an intelligent recommendation system to help users discover books they might enjoy. By leveraging user ratings and book metadata, the system can provide personalized suggestions through:
- **Content-Based Filtering:** Using metadata like book title, genre, author, and description.
- **Collaborative Filtering:** Based on user ratings and preferences using the SVD algorithm from the `Surprise` library.

## 🛠️ Features

1. **Content-Based Recommendations:** Suggest similar books using TF-IDF and cosine similarity.
2. **Collaborative Filtering:** Predict user ratings for books using the SVD algorithm.
3. **Dynamic Hybrid Model:** Combines both methods for a tailored recommendation experience.
4. **Exploratory Data Analysis (EDA):** Visualizations to understand book trends, ratings distribution, and popular genres/authors.

---

## 📂 Dataset

### Sources:
1. **Books Metadata:** A dataset containing information about 70,000 books (e.g., title, author, genre, description, and ratings).
2. **User Ratings:** A dataset of user-book interactions with columns `user_id`, `book_id`, and `rating`.

### Sample Data Preview
#### Books Dataset:
| book_id | title                 | author        | genre          | rating | desc            |
|---------|-----------------------|---------------|----------------|--------|-----------------|
| 3868    | The Catcher in the Rye | J.D. Salinger | Fiction, Classics | 4.1    | A story about...|

#### Ratings Dataset:
| user_id | book_id | rating |
|---------|---------|--------|
| 101     | 3868    | 5      |

---

## 🛠️ Setup & Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/abdelrahman-ehab/book-recommendation-system.git
   cd book-recommendation-system
Usage
1. EDA & Visualization
Run the EDA section to analyze trends in book ratings, genres, and author popularity.

2. Content-Based Recommendations
Call the function get_content_based_recommendations(user_id, tfidf_matrix, final_books) to get book recommendations for a user based on metadata.

3. Collaborative Filtering Recommendations
Call the function get_collaborative_recommendations(user_id, model, trainset) to predict top-rated books for a user.

4. Hybrid Recommendations
Implement a weighted hybrid system by combining content-based and collaborative recommendations dynamically.

## Visualizations

Ratings Distribution: A histogram showcasing how books are rated.
Top Genres & Authors: Bar plots highlighting the most popular genres and authors.
Box Plots: Visualize ratings distribution for the top 20 authors.

## Results

Content-Based Filtering:
Extracted book features using TF-IDF Vectorization.
Computed similarity using cosine similarity to recommend books.
Collaborative Filtering:
Modeled user-item interactions using the Surprise library's SVD algorithm.
Predicted unseen ratings for books and recommended the highest-scoring ones.
Hybrid Model: Balanced both approaches for comprehensive recommendations.

## Contributing
Contributions are welcome! Please open an issue or submit a pull request for any feature requests or improvements.



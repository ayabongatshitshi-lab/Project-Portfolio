**Book Recommendation System using K-Nearest Neighbors**

This project implements a book recommendation algorithm using the K-Nearest Neighbors (KNN) approach. The model leverages the Book-Crossings dataset (hosted in freecodecamp's website), containing 1.1 million ratings (scale 1–10) for 270,000 books by 90,000 users.

The goal is to provide a list of 5 books similar to a given book, based on rating patterns. Using NearestNeighbors from sklearn.neighbors, the algorithm calculates distances between book instances to determine similarity. To ensure statistically meaningful recommendations, the dataset is filtered to remove users with fewer than 200 ratings and books with fewer than 100 ratings.

A function get_recommends(book_title) returns a list containing the target book and five recommended books along with their similarity distances. This project demonstrates the application of KNN in recommendation systems, handling large-scale user-item rating data, and filtering sparse datasets to improve prediction quality.


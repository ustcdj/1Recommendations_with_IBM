# Recommendations with IBM

- [Table of Contents](#Table_of_Contents)
  - [1. Introduction](#1-Introduction)
  - [2. File Descriptions](#2-file-descriptions)
  - [3. Acknowledgements](#3-Acknowledgements)

## 1. Introduction

This project is to analyze the interactions that users have with articles on the IBM Watson Studio platform, and make recommendations to them about new articles they might like.

Three approaches were performed to make recommendations.
1. Rank Based Recommendations
Find the most popular articles simply based on the most interactions. Since there are no ratings for any of the articles, I assume the articles with the most interactions are the most popular. These are then the articles we might recommend to new users.

2. User-User Based Collaborative Filtering
In order to build better recommendations for the users of IBM's platform, I checked users that are similar in terms of the items they have interacted with. These items could then be recommended to the similar users. This approach could provide more personal recommendations for the users.

3. Matrix Factorization
Finally, I used machine learning approach to building recommendations. The data was split into training dataset and testing dataset. Using the user-item interactions, I built out a matrix decomposition from training dataset. Using the decomposition and testing dataset, I calculated predicted user-item interactions of testing dataset. I came up with an optimal number of latent features of 248. With this many latent features, the accuracies for training and testing datasets are 92%.

## 2. File Descriptions

In the Project Workspace, you'll find a data set containing real messages that were sent during disaster events.

* `data`
  * `articles_community.csv` -  data of articles infomation
  * `user-item-interactions.csv` - data of interactions of user and articles
* `user_item_matrix.p` - saved user_item_matrix pickle file
* `Recommendations_with_IBM.ipynb` - the project notebook
* `Recommendations_with_IBM.html` - the project notebook in html

## 6. Acknowledgements

Special thanks to IBM Watson Studio for providing the dataset and to Udacity for creating this project.

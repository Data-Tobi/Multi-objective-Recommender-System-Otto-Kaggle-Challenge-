# Multi-objective-Recommender-System-Otto-Kaggle-Challenge

The goal of this project is to predict clicks, add to carts, and orders of users in the OTTO online shop.
The available data contains 12 million user sessions with product IDs, events (clicks, add to carts, orders) and timestamps, but no meta data.

The score is evaluated on Recall@20 for each action type (weight-averaged), which means that the Recall is one, if one of our twenty predictions was true and zero otherwise.

score=0.10R_clicks+0.30R_carts+0.60R_orders

We achieved a score of 0.54 by using Word2Vec and a score of 0.57 by building a co-visitation matrix.
For each product ID, we
- Create an entry in a matrix
- Find all other products, that got clicked together with this ID
- Count the appearances of those products and store the result in the matrix

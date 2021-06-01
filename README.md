# Recommendation system

Problem Statement
For this project I will be making movie recommendations based on the MovieLens (https://grouplens.org/datasets/movielens/latest/) dataset from the GroupLens research lab at the University of Minnesota. I will be using the "small" dataset containing 100,000 user ratings.

My main goal is to build a model that provides top 5 movie recommendations to a user, based on their ratings of other movies. Also, my recommendation system will be using collaborative filtering as the primary mechanism and content-based filtering to address the cold start problem.

Collaborative filtering
To build a system that can automatically recommend items to users based on the preferences of other users,I will need to answer these questions:

How to determine which users or items are similar to one another?

Given that I know which users are similar, how do I determine the rating that a user would give to an item based on the ratings of similar users?

How do I measure the accuracy of the ratings you calculate?


# Recommendation system

### Problem Statement

For this project I will be making movie recommendations based on the MovieLens (https://grouplens.org/datasets/movielens/latest/) dataset from the GroupLens research lab at the University of Minnesota. I will be using the "small" dataset containing 100,000 user ratings.

In this project, my main goal is to build a model that provides top 5 movie recommendations to a user, based on their ratings of other movies. Also, my recommendation system will be using collaborative filtering as the primary mechanism and content-based filtering(technique that uses similarities in features to make decisions) to address the cold start problem.

Recommendation engines that run on collaborative filtering recommend each item based on user actions. The more user actions an item has, the easier it is to tell which user would be interested in it and what other items are similar to it. As time progresses, the system will be able to give more and more accurate recommendations.

Cold start problem simply means that a recommendation engine meets a new visitor for the first time. Because there is no history about a user, the system doesn’t know the personal preferences of the user. Getting to know the users is crucial in creating a great user experience for them.

### My project consists of 2 main sections:

Section 1 includes cold start developing and building a recommender system from scratch.

In Section 2 I used Surprise library to build the recommender system.

### Section 1

First part of this section consists of - Cold start developing where I will be defining a function which returns 5 best films(cold start problem happens when new users or new items arrive in e-commerce platforms and it makes it difficult to detact personal preferences of the user).Eventually, I want to have a list of movies which have both high average ratings and high number of ratings. I will start with merging two datasets to find the average ratings and the number of ratings for a movie and then by looking at distribution of users rating decide if I have to define a threshold.

In the second part of this section - Building recommender system I will be building a simple recommender system which will focus on movie genres which are the most similar to those viewed by the users.In case if there will not be any information about a movie genre my recommender system will use a cold start.

In the third part of this section - Comparison, I will be comparing results of the recommender system and the cold start but to do that I will build a metric by defining a function which will return a number of movies in recommendations that user watched before.

### Section 2
Surprise package for collaborative filtering.
I will use the Surprise library that provides various ready-to-use powerful prediction algorithms to evaluate its RMSE (Root Mean Squared Error) and FCP(Fraction of Concordant Pairs) on the MovieLens dataset. In this section I will use 3 models: KNN( K nearest neighbors), SVD(Singular Value Decomposition) and NMF(Non-negative matrix factorization). All these methods have different approaches of performance evaluation and that is why I have decided to use them.

FCP. It is the fraction of concordant pairs among all the pairs (sum over all users). Suppose a user has rated n products, then there are  𝑛(𝑛−1)2  unique pairs of ratings. If product A receives a higher rating than product B from a user and the model predicts the same, A and B are a concordant pair, otherwise a discordant pair.

KNN. Helps determine if a data point will be part of one class or another. It looks at the neighboring data points to determine what this new data point will fall into. For example, it is determining if someone will be a republican or democrat based on their income and age.

SVD. Its purpose is to reduce a dataset containing a large number of values to a dataset containing significantly fewer values, but which still contains a large fraction of the variability present in the original data.

NMF. It is useful when there are many attributes and the attributes are ambiguous or have weak predictability. By combining attributes, NMF can produce meaningful patterns, topics, or themes.

### Conclusion
The "small"(100,000 user ratings) MovieLens dataset was used to build the recommender system. This dataset contains movie ratings and movie specific data relevant for my research. After doing an exploratory data analysis I noted that a lot of movies were produced during 1990 and 2000. Also,according to the dataset Drama, comedy and thriller are the most popular genres.

I developed a cold start and got a list of top 5 movies based on average ratings given by users : The Shawshank Redemption, The Godfather, The Fight Club, Cool Hand Luke and Dr. Strangelove or: How I Learned to Stop Worrying and Love the Bomb.Also, I built a recommender but its relsults were worse than the cold start's.

My last part of the project consists of implementing surprise package for collaborative filtering where I used 3 methods KNN, SVD, and NMF methods to evaluate RMSE and FCP on the MovieLens dataset.

The SVD model shows the best results and was able to predict new ratings with a RMSE of 0.87 and FCP of 0.66.



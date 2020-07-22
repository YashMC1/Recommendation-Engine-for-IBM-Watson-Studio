**Introduction**

For this project you will analyze the interactions that users have with articles on the IBM Watson Studio platform, and make recommendations to them about new articles you think they will like.

In order to determine which articles to show to each user, you will be performing a study of the data available on the IBM Watson Studio platform. You can create your own account to become a part of their community, and get a better understanding of their data by creating an account on the platform here. Your Tasks

The project will be divided into the following tasks:
**I. Exploratory Data Analysis**

Before making recommendations of any kind, you will need to explore the data you are working with for the project. Dive in to see what you can find. There are some basic, required questions to be answered about the data you are working with throughout the rest of the notebook. Use this space to explore, before you dive into the details of your recommendation system in the later sections.
**II. Rank Based Recommendations**

To get started in building recommendations, you will first find the most popular articles simply based on the most interactions. Since there are no ratings for any of the articles, it is easy to assume the articles with the most interactions are the most popular. These are then the articles we might recommend to new users (or anyone depending on what we know about them).
**III. User-User Based Collaborative Filtering**

In order to build better recommendations for the users of IBM's platform, we could look at users that are similar in terms of the items they have interacted with. These items could then be recommended to the similar users. This would be a step in the right direction towards more personal recommendations for the users. You will implement this next.
**IV. Content Based Recommendations**

This content based recommender looks at the articles the user has interacted with. It goes through each article and using he NLTK library, finds the most common words in the titles of each article.
Based on these most common words, the recommender looks at the sums of words relevant words in the title of each article, and based on the number of matches in the titles as well as the general popularity of the article it gives back the best recommendations.
If the user has not read any articles yet, then we can't really give any content based recommendations, and just return back some of the most popular articles.
There is a lot of potential improvement and optimization for this recommender. For example one could construct a custom NLTK corpus which would filter out article words. Currently I use a combination of a couple standard NLTK corpora. Furthermore, If df_content had information for all articles we could expand this recommender to look through not only the title but also the body of the articles.
**V.SVD - Matrix Factorization**

Finally, you will complete a machine learning approach to building recommendations. Using the user-item interactions, you will build out a matrix decomposition. Using your decomposition, you will get an idea of how well you can predict new articles an individual might interact with. You will finally discuss which methods you might use moving forward, and how you might test how well your recommendations are working for engaging users.
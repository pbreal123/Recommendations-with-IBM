# Data Scientist Nanodegree Udacity
## Recommendations With IBM project

#Overview
In this project, we analyze user interactions with articles on the IBM Watson Studio platform and create personalized recommendations for users. The goal is to explore several recommendation techniques, such as rank-based recommendations, collaborative filtering, content-based filtering, and matrix factorization.

#Project Motivation
The aim is to recommend articles to users based on their past interactions, using the available data from the IBM Watson Studio platform. Since there are no explicit ratings (like thumbs up/down), the recommendation system will infer user preferences based on interactions such as views, clicks, and reads.


In order to determine which articles to show to each user, It will be performing a study of the data available on the [IBM Watson Studio platform](https://dataplatform.cloud.ibm.com/).
### Libraries
<ul>
  <li>python 3.7 and above</li>
  <li>pandas</li>
  <li>numpy</li>
  <li>matplotlib</li>
  <li>pickle</li>
  <li>re</li>
  <li>nltk</li>
  <li>sklearn</li>
  <li>jupyter</li>
</ul>

### Data
<p>2 .csv files</p>
<ul>
  <li>user-item-interactions.csv: Interactions between users and articles.</li>
  <li>articles_community.csv: Contents of articles.</li>
</ul>

#1. Exploratory Data Analysis (EDA)
The first step in the project is to explore the data. This involves:

Loading and cleaning the datasets.
Checking for missing or inconsistent data.
Summarizing the datasets with descriptive statistics.
Visualizing patterns in user activity and article popularity.
Through EDA, we will answer questions such as:

How many unique users and articles are present in the datasets?
What is the distribution of interactions across users and articles?
Which articles are the most popular based on user interactions?
#2. Rank-Based Recommendations
As a simple starting point, we will recommend the most popular articles, assuming that articles with more interactions are more likely to be of interest to users. The steps are:

Count the interactions for each article.
Sort articles by interaction count.
Recommend the top articles to users who haven't interacted with them.
This serves as a baseline model for comparison with other techniques.

#3. User-User Collaborative Filtering
This method recommends articles based on user similarity. The basic idea is to find users who have interacted with similar articles and suggest articles that these similar users liked. Key steps include:

Building a user-item interaction matrix.
Calculating user similarity using cosine similarity or other metrics.
Recommending articles that similar users interacted with but the target user hasn’t.
#4. Content-Based Recommendations
Content-based filtering uses the features of the articles themselves to make recommendations. This is done by analyzing the textual content of articles and suggesting similar articles based on their content. Using Natural Language Processing (NLP), we will:

Extract features from article text (e.g., using TF-IDF).
Calculate the similarity between articles.
Recommend articles with similar content to those the user has already interacted with.
#5. Matrix Factorization
Matrix factorization techniques, like Singular Value Decomposition (SVD), decompose the user-item interaction matrix into lower-dimensional matrices. This method allows us to predict which articles a user may interact with in the future based on past behavior. The steps include:

Building a user-item interaction matrix.
Applying matrix factorization techniques (e.g., SVD).
Predicting missing interactions and recommending articles to users.
Evaluation & Discussion
At the end of the project, we compare the performance of the different recommendation methods:

Rank-based Recommendations: Simple, but not personalized.
Collaborative Filtering: Personalizes recommendations based on user similarity.
Content-Based Filtering: Uses article content to recommend similar articles.
Matrix Factorization: Attempts to predict missing interactions using latent factors.
We will also discuss how to evaluate the effectiveness of these methods, exploring metrics such as precision, recall, and user engagement.

#Conclusion
This project showcases various approaches to building an article recommendation system, each with its strengths and limitations. By comparing the different methods, we gain insights into how well each approach performs in providing meaningful recommendations to users.

#Credits
This dataset and project were provided by Udacity as part of the Data Scientist Nanodegree.
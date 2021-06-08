# Recommendation-Systems
Recommendation Engine filter out the poducts that a paticular customer would be interested in or would buy based on his/her previous buying history but if the customer is new then this method will fail as we have no previous data from the customer.So,to tackle this issue different methods are used,for example oftern the most popular products are recommended.This recommendations would not be must accurate as they are not customer dependent and are same for all new customers.

So  recommndation engines above are:
1) Collabrative Recommender System
2) Content based Recommender System
3) Popularity based Recommender System

Content Based Filtering
In this recommender system the content of the movie (overview, cast, crew, keyword, tagline etc) is used to find its similarity with other movies. Then the movies that are most likely to be similar are recommended.

  Plot description based Recommender
  We will compute pairwise similarity scores for all movies based on their plot descriptions and recommend movies based on that similarity score. The plot 
  description is given in the overview feature of our dataset
  we'll compute Term Frequency-Inverse Document Frequency (TF-IDF) vectors for each overview.
  We see that over 20,000 different words were used to describe the 4800 movies in our dataset.

  With this matrix in hand, we can now compute a similarity score. There are several candidates for this; such as the euclidean, the Pearson and the cosine 
  similarity scores. There is no right answer to which score is the best. Different scores work well in different scenarios and it is often a good idea to 
  experiment with different metrics.

  We will be using the cosine similarity to calculate a numeric quantity that denotes the similarity between two movies. We use the cosine similarity score since it 
  is independent of magnitude and is relatively easy and fast to calculate. Mathematically, it is defined as follows:
  ![image](https://user-images.githubusercontent.com/56895070/121231318-e6ae1d80-c8ad-11eb-8883-4b2f7406211e.png)


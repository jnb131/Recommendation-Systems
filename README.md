## Recommendation-Systems
Recommendation Engine filter out the poducts that a paticular customer would be interested in or would buy based on his/her previous buying history but if the customer is new then this method will fail as we have no previous data from the customer.So,to tackle this issue different methods are used,for example oftern the most popular products are recommended.This recommendations would not be must accurate as they are not customer dependent and are same for all new customers.

So  recommndation engines above are:
1) Collabrative Recommender System
2) Content based Recommender System
3) Popularity based Recommender System

# Demographic Filtering 

  we need a metric to score or rate movie
  Calculate the score for every movie
  Sort the scores and recommend the best rated movie to the users.
  We can use the average ratings of the movie as the score but using this won't be fair enough since a movie with 8.9 average rating and only 3 votes cannot be 
  considered better than the movie with 7.8 as as average rating but 40 votes. So, I'll be using IMDB's weighted rating (wr) which is given as :-
  
  
   ![image](https://user-images.githubusercontent.com/56895070/121231713-5b815780-c8ae-11eb-87d5-9a36994fedc2.png)  

   where,

  v is the number of votes for the movie;
  m is the minimum votes required to be listed in the chart;
  R is the average rating of the movie; And
  C is the mean vote across the whole report
  We already have v(vote_count) and R (vote_average) and C can be calculated as

# Content Based Filtering
In this recommender system the content of the movie (overview, cast, crew, keyword, tagline etc) is used to find its similarity with other movies. Then the movies that are most likely to be similar are recommended.

  # Plot description based Recommender
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
            
  # Credits, Genres and Keywords Based Recommender
  It goes without saying that the quality of our recommender would be increased with the usage of better metadata. That is exactly what we are going to do in this 
  section. We are going to build a recommender based on the following metadata: the 3 top actors, the director, related genres and the movie plot keywords.

  From the cast, crew and keywords features, we need to extract the three most important actors, the director and the keywords associated with that movie. Right  
  
  The next steps are the same as what we did with our plot description based recommender. One important difference is that we use the CountVectorizer() instead of 
  TF-IDF. This is because we do not want to down-weight the presence of an actor/director if he or she has acted or directed in relatively more movies. It doesn't 
  make much intuitive sense.now, our data is present in the form of "stringified" lists , we need to convert it into a safe and usable structure
  We will use the same score above to find similarity and output the top similarity
  
# Collabrative Filtering
  Using K Nearest Neighbour we will find the most similar users in item-item recommendation system where the ratings on item(int this case movies) will be given to 
  on users which are similar to them based on the rating given on the same movies by the other most smilar users this more optimal than user-user which helps to 
  capture the dynamic nature of the user
  For similarity we can use cosine similarity or pearson correlation
  
  ![image](https://user-images.githubusercontent.com/56895070/121233111-eadb3a80-c8af-11eb-9194-8bd7f0d92970.png)

# once-upon-a-time

My NLP project was to analyze Disney movie scripts and their original stories. I wanted to find relationships between 
the scripts and original stories and to create a book/movie recommender. To do that, I first had to collect my scripts
and stories off the internet. I then tokenized on the sentence level for sentiment analysis and on the word level for 
topic modeling and for creating word embeddings using Word2Vec and PCA. Together with my sentiment analysis and topic
modeling, I created a recommendation system using Flask.

What I found through my sentiment analysis was that the Winnie the Pooh movie script and its original story was
the most similar out of the 16 other pairs of books/movies. The Hunchback of Notre Dame book/movie pair came out
to be the most dissimilar. This might be because the original Hunchback of Notre Dame was a thick gothic novel while 
the movie is a short and happier version of the book. 

A related finding was discovered using word embeddings. Word embeddings are used to reconstruct linguistic 
contexts of words. I looked at how spread out the main character names were from each other in the books and in the 
movies. I also looked at how spread out the main character names were from the words ‘love’ and ‘happy’. I found that
in the original stories, the main character names were more spread out from each other, with some closer to the words
love and happy than others. Quasimodo, the hunchback from the Hunchback of Notre Dame was the farthest from the other
characters and the words love and happy. However, word embeddings for the movie scripts showed that the main character
names were clustered closer to each other and to the words love and happy. This may show that the movies were more 
similar to each other and possible sugar coated the original stories.

The recommendation system that I talked about earlier was created with topic modeling and sentiment analysis.
I used NMF to get the topic weights for each story and movie and the dynamic time warping distances for each 
movie or book compared to another movie or book based on the change in sentiment over time. Using cosine similarity
on the topic weights, I was able to tell how similar each movie or book is to another movie or book. The dynamic 
time warping distance applied on the change in sentiment over time tells me how similar a movie or book feels compared
to another movie or book. The end user gets to choose a book or movie they enjoyed and also gives a number to represent
how similar they want the recommended book or movie to feel in terms of plot and how similar in topic they want and the
recommender would provide a book or a movie they should watch or read next.

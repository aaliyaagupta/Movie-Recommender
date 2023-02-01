# Movie-Recommender
A recommender system which will recommend movies based on the plot description and the genre. It’s a content based recommendation system.
The algorithm rates the items and shows the user the items that they would rate highly. An example of recommendation in action is when you visit Netflix and you notice that some items are being recommendeded to you. They’re also used by Spotify and other music apps.


# Types of Recommender systems


1.Content based systems: I have used this recommendation system in the project.
It uses metadata such as genres, producer, actors, musicians, years to recommend items say movies or music. Such a recommendation system would be for instance recommending Lord of the rings because someone watched The Hobbit.
Similarly it can suggest music on basis of what genre or artist you listen to.
Content based systems are based on the idea that if you liked a certain item you are most likely to find something similar to it.

2.User based collaborative filtering: In this model products are recommended to a user based on the fact that the products have been liked by users similar to the user.
 If Isha and Simran like the same movie then a new movie releases which Isha likes will also be suggested to Simran.


3.Item Based collaborative filtering: These systems identify similar items based on users’ previous ratings. For example if users A,B,C gave a 5 star rating to books X ,Y then when a user D buys book Y they also get a recommendation to purchase book X and Y as similar based on the ratings.

# DATASET
In this project the datasets used is from the IMDB site, and movie ids help gather much of this data come from one or two Kaggle projects. 
 The dataset contains the top 250 movies from IMDB with 27 attributes like Title, Director, Genre, Plot, Ratings, etc.
 
 
 # Tools Used

Libraries used in the project are
Pandas- Pandas is an open-source library that is made mainly for working with relational or labeled data both easily and intuitively. It provides various data structures and operations for manipulating numerical data and time series. This library is built on top of the NumPy library. Pandas is fast and it has high performance & productivity for users.

Sklearn- Scikit-learn is the most useful and robust library for machine learning in Python. It provides a selection of efficient tools for machine learning and statistical modeling including classification, regression, clustering and dimensionality reduction via a consistence interface in Python.
 
nltk- is a toolkit build for working with Natural Language Processing in Python. It provides us various text processing libraries with a lot of test datasets. A variety of tasks can be performed using NLTK such as tokenizing, parse tree visualization. In this article, we will go through how we can set up NLTK in our system and use them for performing various NLP tasks during the text processing step.

re- Regular Expression. A regular expression specifies a set of strings that matches it; the functions in this module let you check if a particular string matches a given regular expression 


# Methodology

After having imported the libraries, we start with the plots of the movies given in the dataset, we tokenize the plot of the movies. Word tokenization is the process of splitting a large sample of text into words. This is a requirement in natural language processing tasks where each word needs to be captured and subjected to further analysis like classifying and counting them for a particular sentiment etc.

Next we preprocess all the other attributes of the dataset such as the genre, title, directors, actors etc. 
For the next step, which is feature extraction I have used the tf idf vectorisation in python which will be imported from the sklearn library.
  
The tf–idf vectorizor is a mathematical statistic which gives proportionally to the number of times a word shows up in the document. It is planned to reflect how significant a word is to the document.


Term Frequency (tf) - It gives us the recurrence of the word in each report in the collection. It is the proportion of the number of times the word shows up in a report contrasted with the all-out the number of words in that record. It increments as the quantity of events of that word inside the record increments.


Inverse Data Frequency (idf) - It is used to figure the heaviness of uncommon words over all reports in the collection. The words that happen seldom in the corpus have a high IDF score.
                                               

Using the module we make a cosine matrix to find the similarity between the words in the plot of the movie. A commonly used approach to match similar documents is based on counting the maximum number of common words between the documents.
So if some movie’s plot is similar to some other movie we will have a higher similarity score and based on that we are going to recommend the movies
We make an index data frame to get the title, and make a function for getting the index of the movie based on which we get the similarity matrix.
After this, the scores are to be calculated using the matrix, higher the score , will be the top movie we can recommend
We ll have a score in terms of the dataframe



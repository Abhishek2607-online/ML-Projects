Twitter Sentimental Analysis



Name: -         Abhishek Negi
U. Roll No.: -  2012467
Section: -      C




PROBLEM STATEMENT:-
  
The objective of this task is to detect hate speech in tweets. For the sake of simplicity, 
we say a tweet contains hate speech if it has a racist or sexist sentiment associated with it. So, the task is to classify racist or sexist tweets from other tweets.





ABSTRACT:-

Formally, given a training sample of tweets and labels, where label ‘1’ denotes the tweet is racist/sexist and 
label ‘0’ denotes the tweet is not racist/sexist, your objective is to predict the labels on the given test dataset. 
The evaluation metric for this practice problem is F1-Score.





METHODOLOGY:-
  
We will use machine learning techniques like Natural Language Processing to solve this problem problem, 
we will preprocess the data with some standard technique of NLP and after that we will train our data.






DATASET: -

The data has 3 columns id, label, and tweet. label is the binary target variable and tweet contains the tweets that we will clean and preprocess.
There are two files train and test, train data contain 3(id, label, tweet) column and 31962 rows and test data contain 2 column(id, tweet) and 49159 rows 
Label are 0 and 1:
0 means positive tweet and 1 means negative tweets. 






ALGORITHMS/TECHNIQUES:-

In this project, Logistic Regression (RF) will be implemented and the learning algorithms will be implemented by sklearn toolbox in this project.
Logistic Regression:-
Logistic regression is a linear model for classification. In this model, the output of a single trial can be interpreted as class probability, 
which is generated by a logistic function or sigmoid function. sklearn provides a function called LogisticRegression(). 
One typical tunable hyper parameter is” C”, which is the inverse of regularization strength. 
The advantage of logistic regression is that the training and predicting speed is very fast.
This is done in two ways both are below: -
Building model using Bag-of-Words features
•	Bag-of-Words is a method to represent text into numerical features. 
Building model using TF-IDF features
•	This is another method which is based on the frequency method but it is different to the bag-of-words approach in the sense that it takes into account, not just the occurrence of a word in a single document (or tweet) but in the entire corpus.






HOW AND WHAT I DID:-

Firstly, I learned basics of Machine learning from 2 courses namely: -
1.	Machine Learning by Andrew Ng
2.	Machine Learning (Udemy Course)
Then I started Kaggle Machine Learning course to implement things practically.
This project was part of that course which helped me a lot to complete this project with less difficulty and errors.





Pre-processing phase: -

•	The Tweets are masked as @user due to privacy concerns. So, these Twitter handles are not important to us we will remove this.
•	We will also remove numbers and special character.
•	Most of the smaller words do not add much value. For example, ‘pdf’, ‘his’, ‘all’. So, we will try to remove them as well from our data.
•	Once we have executed the above three steps, we can split every tweet into individual words or tokens which is an essential step in any NLP task.
•	Removing Twitter Handles (@user)
•	Removing Punctuations, Numbers, and Special Characters
•	Removing Short Words
•	Tokenization: - splitting string into tokens
•	Stemming: - cutting some words for e.g.: - play, played, playing as play





EDA: -

EDA is done using worldcloud it is a NLP library.
A wordcloud is a visualization wherein the most frequent words appear in large size and the less frequent words appear in smaller sizes.
Using worldcloud to do EDA on the things mentioned below: -
•	Words in non-racist/sexist tweets
•	Racist/Sexist Tweets
•	Understanding the impact of Hashtags on tweets sentiment
•	Extracting Features from Cleaned Tweets (To analyse a pre-processed data, it needs to be converted into features. 
Depending upon the usage, text features can be constructed using assorted techniques – Bag-of-Words, TF-IDF, and Word Embeddings.)






Model Fitting: -

•	Data set is splitted into train and test using train-test-split (method of sklearn.model_selection)
•	Than LogisticRegression model is fitted to the data set and output is predicted.
•	Then output is compared with the validation data and f1-score is calculated.
•	Similarly it is done with second technique.




RESULT:-
We learned how to approach a sentiment analysis problem. 
Bag of words result f1 score-0.53
TF-IDF method result f1 score-0.54




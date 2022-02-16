# <p align = 'center'>Amazon Sentiment Analysis</p>

<p align = 'center'> <img width="600" img height="200" src = https://github.com/siddh30/Amazon-Sentiment-Analysis/blob/master/amazon_logo.png </p>
  
## ***Project Overview***
In this project we carry out Sentimental Analysis on Amazon's Books Dataset based on reviews on a million books and predict whether this review is 'Positive', 'Neutral', 'Negative'. Apart from reviews we have also predicted their individual ratings. We have four different approaches to our project.


## ***Dataset Description***
The Amazon's Books Dataset containing more than a  million books, thier reviews and their ratings.


## ***Our Apporaches***
Approach 1: Using spaCy for tokenization, Lemmatization and Removing stopwords and using scikit-learn to build our models for different batches of data and using Ensemble Techniques to create an aggregate prediction result.

Approach 2: Using NLTK for tokenization, Lemmatization and Removing Stop words and using scikit-learn to build our models for different batches of data.

Approach 3: Using a custom-built Naïve Bayes model.

Approach 4: Handling Big Data using pyspark.


  
## ***Our Results***

Overall, implementing logistic regression (0.89605) using SPACY provided the highest accuracy and the least compilation time and it was the most feasible machine learning model for Approach 1. We also implemented ensemble learning and though Random Forest did provide a higher accuracy (0.88475) as compared to Decision Trees (0.84955), it did not improve the overall performance.

In our second approach, amongst Logistic regression, Decision Trees and Support Vector Machines, the highest accuracy of 0.8644 was achieved by Logistic Regression when samples of our review_body feature were passed through Countvectorizer() with ngram=(1,2) and the classifier having parameters like maximum iteration=500, C=0.1, random_state=40, and solver=’newton-cg.’ On the flip side, our KNN model was comparatively faster but achieved a score of 0.578.

Our custom-built Naïve Bayes model in approach 3 achieved an accuracy of 0.909 which is the highest among all our approaches. However this model has a large computational time.

In our last approach we find ways to deal with our dataset which consists of more than 3 million records of books and reviews. Using Pyspark, we trained our model (logistic regression) and it achieved an accuracy of 66.667% on our test data. Another way of dealing with big data was to construct a custom loop which created models and generated predictions for different batches of data. Accuracies with one of these batches hit above 90%.


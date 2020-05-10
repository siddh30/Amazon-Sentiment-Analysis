<p>
<p align="center">
<img src="web_logo.png"
     img width="600" img height="200"
     alt="Markdown Monster icon"
      />
</p>
</p>. 

## Introduction
Sentiment analysis is a text analysis method that detects polarity (e.g. a positive or negative opinion) within text, whether its a whole document, paragraph, sentence, or a clause.

Understanding people’s emotions is essential for businesses since customers are able to express their thoughts and feelings more openly than ever before. By automatically analyzing customer feedback, from survey responses to social media conversations, brands are able to listen attentively to their customers, and tailor products and services to meet their needs.

In this project we carry out Sentimental Analysis on Amazon's Books Dataset based on reviews on a million books and predict whether this review is 'Positive', 'Neutral', 'Negative'. We have four different approaches to our project.

## Our Data
The Amazon's Books Dataset containing a million books, thier reviews and their ratings.

## Our Approaches 
Approach 1: Using spaCy for tokenization, Lemmatization and Removing stopwords and using scikit-learn to build our models for different batches of data and using Ensemble Techniques to create an aggregate prediction result.

Approach 2: Using NLTK for tokenization, Lemmatization and Removing Stop words and using scikit-learn to build our models for different batches of data.

Approach 3: Using a custom-built Naïve Bayes model

Approach 4: Handling Big Data

## Our Results
1. Overall, implementing logistic regression (0.89605) using SPACY provided the highest accuracy and the least compilation time and it was the most feasible machine learning model for Approach 1. We also implemented ensemble learning and though Random Forest did provide a higher accuracy (0.88475) as compared to Decision Trees (0.84955), it did not improve the overall performance.

2. In our second approach, amongst Logistic regression, Decision Trees and Support Vector Machines, the highest accuracy of 0.8644 was achieved by Logistic Regression when samples of our review_body feature were passed through Countvectorizer() with ngram=(1,2) and the classifier having parameters like maximum iteration=500, C=0.1, random_state=40, and solver=’newton-cg.’ On the flip side, our KNN model was comparatively faster but achieved a score of 0.578. 

3. Our custom-built Naïve Bayes model in approach 3 achieved an accuracy of 0.909 which is the highest among all our approaches. However this model has a large computational time.

4. In our last approach we find ways to deal with our dataset which consists of more than 3 million records of books and reviews. Using Pyspark, we trained our model (logistic regression) and it achieved an accuracy of 66.667% on our test data. Another way of dealing with big data was to construct a custom loop which created models and generated predictions for different batches of data. Accuracies with one of these batches hit above 90%.





<p>
<p align="center">
<img src="web_logo.png"
     img width="600" img height="200"
     alt="Markdown Monster icon"
      />
</p>
</p>. 

## Introduction
Sentiment analysis is a text analysis method that detects polarity (e.g. a positive or negative opinion) within text, whether a whole document, paragraph, sentence, or clause.

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
1. Overall, implementing logistic regression (0.89605) using SPACY provided the highest accuracy and the least compilation time and it was the most feasible machine learning model for Approach. We have also implemented ensemble learning and though Random Forest did provide a higher accuracy (0.88475) as compared to Decision Trees (0.84955), it did not improve the overall performance.

2. In approach 2, amongst Logistic regression, Decision Tree and Support vector the highest accuracy of 0.8644 was achieved   when Bag of words were implemented using Countvectorizer() with ngram=(1,2) with Logistics Regression having parameters maximum iteration=500, C=0.1, random_state=40, and solver=’newton-cg.’ Whereas the KNN model is comparatively faster but was only able to achieve a score of 0.578. 

3. Our custom function of Naïve Bayes implementation in approach 3 was able to achieve highest accuracy score of 0.909 among all the models and in all approaches. But it is highly time complex and took almost a day to train on 200k samples and predict 100k reviews. 

4. In our last approach we find ways to deal with our dataset which consists of more than 3 million records of books and reviews. Using Pyspark, we trained logistic regression and was able to achieve 66.667% accuracy on our test data and using a custom loop we generated batch wise accuracies with one of the batches hitting an accuracy of above 90%. 



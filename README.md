# COVID19-Fake-News-Detection-in-English
## 1. Introduce
During the covid-19 pandemic, a considerable amount of data travels fast worldwide on the net, mainly on the social media platform where people all over the world have constant and easy access to submit materials and posts. A considerable amount of shared news embeds misleading information which affects negatively the cognitive and psychological health of its readers. 
This project exhibits a new approach to detect fake news on Twitter during the Covid-19 period. The proposed method consists of a classification approach that uses new tweets’ features and it is based on natural language processing, machine learning, and deep learning. In this project, we focus on comparing the classification performance of some important and widely used machine learning algorithms, namely Naive Bayes, Logistic Regression, Kernel SVM for news recognition. At the same time, we also tested and evaluated the classification performance of a state-of-the-art deep learning method for solving NLP problems called BERTweet.Thereby we compare and evaluate the real results experience, analyze challenges and propose solutions in the future.
## 2. Dataset
### 2.1 Description of training datasets and evaluation datasets:
A large-scale dataset of 6420 Twitter tweets, of which 3360 tweets labelled as fact make up 52.34% of the training dataset, and there are 3060 tweets labelled as disinformation accounting for 47.66% of the dataset. 
### 2.2 Description of testing dataset:
A large-scale dataset of 2140 Twitter tweets, of which 1120 were labelled as fact, accounted for 52.34% of the training dataset, and 1020 were labelled as fake, accounting for 47.66% of the dataset. 
## 3. Implement
### 3.1 Machine learning model
#### 3.1.1 Data preprocessing
- Encrypt Tweets using the TweetTokenizer function based on the NLTK library, and also use the emoji library to translate the emoticons into text strings (here, each symbol is referred to as a word token. )
- Convert user mentions and weblink/url respectively to @USER and HTTPURL respectively.
- Convert the words in the Tweet into the original word by using the Stemming technique. In the process, we also perform the Lemmatization technique with the desire to create a more accurate and optimal result.
- Vectorization of data using TF-IDF method.
#### 3.1.2 Model training
Using 3 machine learning models: Naive Bayes, SVM, Logistic Regression.
Using deep learning model: COVID-Twitter-BERT (CT-Bert).
#### 3.1.3 Results
Compare results of machine learning models with Lemmatization +Stop Word
Model | Accuracy | Precision | Recall | F1 score
------------ | ------------- | ------------- | ------------- | ------------- 
Naive Bayes | 0.8372 | 0.8422 | 0.8372 | 0.8363
Logistic Regression | 0.9197 | 0.9228 | 0.9229 | 0.9229
SVM | 0.9384 | 0.9386 | 0.9384 | 0.9384

Compare results of machine learning models with Stemming +Stop Word

Model | Accuracy | Precision | Recall | F1 score
------------ | ------------- | ------------- | ------------- | ------------- 
Naive Bayes | 0.8299 | 0.8325 | 0.8299 | 0.8290
Logistic Regression | 0.9229 | 0.9228 | 0.9228 | 0.9228
SVM | 0.9392 | 0.9394 | 0.9392 | 0.9392

Compare results of deep learning models 

Model | Accuracy | Precision | Recall | F1 score
------------ | ------------- | ------------- | ------------- | ------------- 
CT-BERT | 0.9743 | 0.9699 | 0.9813 | 0.9747

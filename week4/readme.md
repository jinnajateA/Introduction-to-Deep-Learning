# Peer-graded Assignment: Week 4: NLP Disaster Tweets Kaggle Mini-Project  

**Problem Description**

This project addresses a natural language processing (NLP) classification task using tweets related to disasters. The objective is to develop a model that can determine whether a given tweet is about a real disaster or not. Accurate classification has practical value in areas such as real-time disaster tracking, emergency response systems, and social media analysis.

The dataset used is the [NLP Disaster Tweets](https://www.kaggle.com/competitions/nlp-getting-started) dataset from Kaggle. It consists of tweets that are labeled to indicate whether they are disaster-related (1) or not (0). The dataset includes:

- `text`: The content of the tweet  
- `keyword`: A keyword from the tweet (optional)  
- `location`: The location from which the tweet was posted (optional)  
- `target`: A binary label where `1` means the tweet is about a disaster, and `0` means it is not  

The data is structured in a tabular format, with rows representing individual tweets and columns providing metadata. The primary feature used in the classification model is the `text` column, as it contains the core content used for prediction.

**Evaluation**

Model performance is evaluated using the **F1 score**, which balances precision and recall. The F1 score is defined as:

F1 = 2 * (precision * recall) / (precision + recall)

Where:

precision = TP / (TP + FP)  
recall = TP / (TP + FN)

- **True Positive (TP)**: Your model predicts 1, and the actual label is also 1 — a correct positive prediction.  
- **False Positive (FP)**: Your model predicts 1, but the actual label is 0 — an incorrect positive prediction.  
- **False Negative (FN)**: Your model predicts 0, but the actual label is 1 — an incorrect negative prediction.  

**Submission File Format**

For each tweet in the test set, your submission should predict `1` if the tweet is about a real disaster, or `0` otherwise. The file must include a header and follow the format below:


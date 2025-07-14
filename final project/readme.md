# DTSA 5511 Introduction to Deep Learning Final Project

### Problem Definition

This project focuses on a **deep learning** task to classify **toxic comments** from online discussion platforms. The goal is to build models that can automatically detect whether a comment contains harmful or abusive content based on natural language text.

This is a **multi-label classification** problem because each comment can belong to more than one toxic category (e.g., both “toxic” and “insult”).

---

### Problem Description

Toxic behavior such as hate speech, insults, or threats is prevalent in online communities. Detecting such content is crucial for:
- **Protecting users from harassment**
- **Maintaining community guidelines**
- **Automating content moderation systems**

This project leverages deep learning models with **pre-trained word embeddings** to detect toxic comments from Wikipedia's talk pages, as provided in the Jigsaw competition dataset.

---

### Problem Topic

- **Type of Learning**: Supervised Learning  
- **Task Type**: Multi-label Text Classification  
- **Target Variables**:  
  - `toxic`, `severe_toxic`, `obscene`, `threat`, `insult`, `identity_hate`  
- **Evaluation Metrics**:  
  - Binary Cross-Entropy Loss  
  - Micro and Macro F1 Score  
  - ROC-AUC (per class and averaged)

---

### About the Data

The dataset is from the [Kaggle Jigsaw Toxic Comment Classification Challenge](https://www.kaggle.com/competitions/jigsaw-toxic-comment-classification-challenge), containing over 150,000 Wikipedia comments labeled with 6 toxicity categories.

#### Key Columns:
- **comment_text**: Raw comment text input  
- **Target Labels**: 0 or 1 for each of the six toxic categories

---

### Text Preprocessing & Embedding

All models in this project use **pre-trained GloVe word embeddings (100-dimensional)**. Key steps include:
- Lowercasing
- Removing punctuation/special characters
- Tokenization and padding (max length: 150)
- Loading GloVe vectors and constructing the embedding matrix
- Initializing a non-trainable embedding layer with GloVe for all models

---

### Deep Learning Models

| Model | Description |
|-------|-------------|
| **ANN** | Baseline feed-forward network using GloVe embeddings + dense layers |
| **RNN** | Recurrent neural network that captures sequential patterns |
| **LSTM** | Long Short-Term Memory model to handle long-term dependencies |
| **Bi-LSTM** | Bidirectional LSTM for capturing context in both directions |

---

### Source

> Kaggle. (2018). *Jigsaw Toxic Comment Classification Challenge*  
> https://www.kaggle.com/competitions/jigsaw-toxic-comment-classification-challenge  

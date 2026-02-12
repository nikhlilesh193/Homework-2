# CS5760 – Natural Language Processing  
## Homework 2  

**Student:** Nikhilesh Katakam  
**700#: 700772365

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## 📌 Overview

This repository contains
Topics covered:

- Naive Bayes Document Classification  
- Harms in Classification  
- Bigram Language Models (MLE)  
- Zero-Probability Problem & Laplace Smoothing  
- Backoff Models  
- Multi-Class Evaluation Metrics  

---

## 📘 Part I – Key Results

### Document Classification
Test document: **“predictable no fun”**

- Positive score = 1/729  
- Negative score = 1/512  

Final Classification: **Negative**

---

### Bigram Model (MLE)

- P(`<s> I love NLP </s>`) = 1/3  
- P(`<s> I love deep learning </s>`) = 1/6  

Model prefers the first sentence (higher probability).

---

### Zero Probability & Smoothing

- MLE gives P(noodle | ate) = 0  
- Using Laplace smoothing:  
  P(noodle | ate) = 1/22  

Smoothing prevents zero probabilities.

---

### Backoff Model

Trigram (You, like, dogs) unseen → probability 0  
Using bigram backoff:

P(dogs | like) = 1/3  

Backoff avoids zero-probability issues.

---

### Evaluation Metrics

Per-Class Precision & Recall:

- Cat: 0.25  
- Dog: 0.444  
- Rabbit: 0.40  

Macro Average = 0.365  
Micro Average = 0.389  

---

## 💻 Programming

Implemented in Python:

- Bigram Language Model  
- Sentence probability computation  
- Confusion matrix metrics (Precision, Recall, Macro, Micro)

Run using:

```bash
python filename.py

# NLP Sentiment Analysis: TF-IDF vs. Sentence-BERT (SBERT)

## Overview
[cite_start]This project explores the "semantic gap" in traditional NLP models by comparing the effectiveness of **TF-IDF** and **Sentence-BERT (SBERT)** in sentiment analysis[cite: 368, 372]. [cite_start]While keyword-centric models like TF-IDF are efficient, they often fail to capture context and intent[cite: 369, 371].

## Features
- [cite_start]**Preprocessing Pipeline**: Includes lowercase conversion, removal of URLs/HTML tags, punctuation stripping, tokenization, stopword removal (NLTK), and lemmatization (WordNet) [cite: 384-397].
- **Model Architectures**:
  - [cite_start]**TF-IDF + Logistic Regression**: Baseline keyword-based model[cite: 400].
  - [cite_start]**SBERT + Logistic Regression**: Uses a pretrained SBERT model as a feature extractor with hyperparameter tuning via GridSearchCV[cite: 401, 404, 406].
- [cite_start]**Comparison Benchmarks**: Evaluated across IMDB movie reviews, straightforward tweets, ambiguous text, and sarcasm[cite: 379, 421, 427, 436].

## Key Findings
- [cite_start]**TF-IDF** outperformed SBERT on standard benchmarks (89.8% vs 82.6% accuracy) where sentiment is expressed explicitly through high-frequency terms [cite: 414-416].
- [cite_start]**SBERT** demonstrated a superior ability to handle ambiguous and linguistically complex scenarios by capturing deep semantic relationships[cite: 430, 447].
- [cite_start]**Sarcasm** remains a significant challenge for both models due to the contradiction between literal text and intended meaning[cite: 449, 450].

## Dataset
- [cite_start]**Primary**: IMDB Movie Reviews (balanced for positive and negative labels)[cite: 379, 382].
- [cite_start]**Initial Experimentation**: Sentiment140 (Twitter data)[cite: 376].

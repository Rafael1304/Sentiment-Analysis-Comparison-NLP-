# NLP Sentiment Analysis: TF-IDF vs. Sentence-BERT (SBERT)

## Overview
This project explores the "semantic gap" in traditional NLP models by comparing the effectiveness of **TF-IDF** and **Sentence-BERT (SBERT)** in sentiment analysis. While keyword-centric models like TF-IDF are efficient, they often fail to capture context and intent.

## Features
- **Preprocessing Pipeline**: Includes lowercase conversion, removal of URLs/HTML tags, punctuation stripping, tokenization, stopword removal (NLTK), and lemmatization (WordNet).
- **Model Architectures**:
  - **TF-IDF + Logistic Regression**: Baseline keyword-based model.
  - **SBERT + Logistic Regression**: Uses a pretrained SBERT model as a feature extractor with hyperparameter tuning via GridSearchCV.
- **Comparison Benchmarks**: Evaluated across IMDB movie reviews, straightforward tweets, ambiguous text, and sarcasm.

## Key Findings
- **TF-IDF** outperformed SBERT on standard benchmarks (89.8% vs 82.6% accuracy) where sentiment is expressed explicitly through high-frequency terms.
- **SBERT** demonstrated a superior ability to handle ambiguous and linguistically complex scenarios by capturing deep semantic relationships.
- **Sarcasm** remains a significant challenge for both models due to the contradiction between literal text and intended meaning.

## Dataset
- **Primary**: IMDB Movie Reviews (balanced for positive and negative labels).
- **Initial Experimentation**: Sentiment140 (Twitter data).

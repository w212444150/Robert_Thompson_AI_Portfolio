# Midterm – CryptoNewsBot Intelligence System

**Course:** ITAI 2373 | Houston Community College  
**Student:** Robert B. Thompson (Team Solo)  
**Instructor:** Prof. Anna Deverakonda  
**Date:** April 1, 2026  
**Midterm Repo:** https://github.com/w212444150/Midterm_NewsBot

---

## Problem Statement

Build an NLP pipeline to classify and analyze crypto and cybersecurity news articles. Crypto markets and cybersecurity teams both face a constant flood of text from news, forums, and threat reports. The system needs to sort, tag, and surface what matters.

## Dataset

250 articles across 5 categories (50 per category):
- Cybersecurity
- Crypto Markets
- Crypto Regulation
- Blockchain Technology
- Threat Intelligence

## System Components

**Classification**  
Multi-category article sorter using spaCy NLP features and scikit-learn classifiers.

**Named Entity Recognition**  
spaCy NER identifies organizations, locations, and financial entities in news text.

**Topic Visualization**  
Word clouds and frequency plots surface dominant themes per category.

**Text Summarization**  
Extractive summarization pulls key sentences from articles by importance.

## Results

- Five-category classifier handled crypto and cybersecurity domain text accurately
- spaCy NER correctly identified organizations, crypto assets, and threat actors
- Word clouds confirmed category-specific vocabulary clusters
- System ran entirely offline with no external API dependencies

## Learning Outcomes

- Domain-specific NLP pipelines outperform generic models on specialized vocabulary
- spaCy's pre-trained models provide fast, accurate NER without additional training
- Visualizations (word clouds, frequency plots) make patterns immediately visible
- Building the midterm first made the final project architecture decisions much cleaner

## Files

- `R_B_Thompson_CryptoNewsBot_Intelligence_System.ipynb` – Full midterm notebook

## Dependencies

```
spacy
scikit-learn
nltk
pandas
numpy
matplotlib
seaborn
wordcloud
plotly
```

```bash
pip install spacy scikit-learn nltk pandas matplotlib seaborn wordcloud plotly
python -m spacy download en_core_web_sm
import nltk; nltk.download('punkt'); nltk.download('stopwords')
```

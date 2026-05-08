# L04 – Text Representation: From Words to Numbers

**Course:** ITAI 2373 | Houston Community College  
**Student:** Robert B. Thompson  
**Instructor:** Prof. Anna Deverakonda  
**Date:** May 2, 2026

---

## Problem Statement

Convert raw text into numerical representations that machine learning models can process. Implement and compare Bag of Words, TF-IDF, and Word2Vec on a movie review dataset.

## Approach

Progressed through three levels of text representation on the same corpus:
1. Bag of Words using `CountVectorizer`
2. TF-IDF weighting using `TfidfVectorizer`
3. Word2Vec dense embeddings using `gensim`

Visualized vocabulary distributions and compared how each method encodes meaning.

## Key Results

- BoW produces sparse matrices where "the" and "ransomware" get equal weight
- TF-IDF down-weights common words and surfaces rare, informative terms
- Word2Vec captures analogy relationships: king − man + woman ≈ queen

## Learning Outcomes

- Bag of Words ignores word order and context; works well for simple classification
- TF-IDF improves on BoW for information retrieval and topic-based tasks
- Dense embeddings from Word2Vec encode semantic similarity in a vector space
- Sparse methods (BoW, TF-IDF) scale better on large corpora; dense embeddings need more compute

## Files

- `R_B_Thompson_L04_ITAI_2373.ipynb` – Text representation lab notebook

## Dependencies

```
nltk
scikit-learn
gensim
matplotlib
seaborn
wordcloud
```

```bash
pip install nltk gensim scikit-learn matplotlib seaborn wordcloud
python -m nltk.downloader punkt stopwords movie_reviews
```

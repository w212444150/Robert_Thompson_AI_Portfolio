# Final – NewsBot 2.0: Advanced NLP Intelligence System

**Course:** ITAI 2373 | Houston Community College  
**Student:** Robert B. Thompson (Team Solo)  
**Instructor:** Prof. Anna Deverakonda  
**Date:** May 2, 2026  
**Domain:** Cryptocurrency and Cybersecurity News

---

## Problem Statement

Extend the midterm CryptoNewsBot into a production-grade, four-module NLP pipeline that classifies, summarizes, tracks sentiment over time, maps entity relationships, and answers natural language queries.

## System Architecture

```
Article Text
     │
     ▼
[Preprocessing]  → tokenization, cleaning, language detection
     │
     ├──► [Classifier]         → category label (crypto / cyber / regulation / market)
     ├──► [Sentiment Tracker]  → VADER score, monthly trend, anomaly detection
     ├──► [Entity Mapper]      → NER + co-occurrence graph
     └──► [Summarizer]         → TF-IDF extractive summary + headline generation
                                        │
                                        ▼
                              [Conversational Interface]
                     Two-stage intent classifier (keyword → ML fallback)
```

## Modules

### 1. Classification
Multi-category article sorter using TF-IDF vectorization and Naive Bayes.  
Domains: crypto markets, cybersecurity, regulation, blockchain, threat intelligence.

### 2. Sentiment Evolution Tracker
VADER compound scoring per article. Monthly time-series tracking. Anomaly detection using z-score threshold of 1.5. Outputs a bullish/bearish signal per article.

### 3. Entity Relationship Mapper
NLTK named entity chunker plus domain keyword matching for threat actors (Lazarus, APT28, Volt Typhoon), crypto assets (Bitcoin, Ethereum, Solana), and regulatory bodies (SEC, CFTC, CISA). Builds a co-occurrence graph to surface which entities appear together.

### 4. Intelligent Summarizer
Extractive summarization using TF-IDF sentence scoring. Three length modes: brief (1 sentence), balanced (2), detailed (4). Multi-article summarization with optional topic focus. Summary quality scoring by coverage and compression ratio.

### 5. Conversational Interface
Two-stage intent classification: keyword matcher for direct queries, ML classifier for ambiguous ones. Graceful fallback for unrecognized queries. Multilingual support via langdetect and Google Translate with local fallbacks.

## Results

- Sentiment tracker detected month-over-month tone shifts in coverage
- Entity mapper linked Lazarus Group and Bitcoin in co-occurrence data
- Summarizer achieved ~30% average compression with readable output
- Conversational interface handled both direct and ambiguous queries correctly

## Learning Outcomes

- A four-module pipeline mirrors real-world NLP system design
- Domain-specific entity lists dramatically improve NER accuracy over generic models
- VADER anomaly detection with z-scores surfaces meaningful signal without labeled data
- Two-stage intent classification balances speed (keyword match) with coverage (ML fallback)

## Files

- `FinalNewsBot2_0_R_Thompson_TeamSolo_ITAI2373.ipynb` – Full final project notebook

## Dependencies

```
nltk
scikit-learn
vaderSentiment
numpy
pandas
matplotlib
langdetect
```

```bash
pip install nltk scikit-learn vaderSentiment numpy pandas matplotlib langdetect
```

```python
import nltk
nltk.download('punkt')
nltk.download('averaged_perceptron_tagger')
nltk.download('maxent_ne_chunker')
nltk.download('words')
nltk.download('vader_lexicon')
```

All external API calls include local fallbacks. Runs fully in Google Colab.

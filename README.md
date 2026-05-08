# L02 – Text Preprocessing and Cleaning

**Course:** ITAI 2373 | Houston Community College  
**Student:** Robert B. Thompson  
**Instructor:** Prof. Anna Deverakonda  
**Date:** May 2, 2026

---

## Problem Statement

Compare NLTK and spaCy preprocessing pipelines and understand how each preprocessing decision affects downstream NLP tasks.

## Approach

Applied tokenization, stemming, lemmatization, and stop word removal to two corpora: product reviews and academic text. Measured vocabulary reduction at each step and evaluated tradeoffs between compression and meaning preservation.

## Results

| Corpus | Vocabulary Reduction |
|--------|---------------------|
| Product reviews | ~61.7% |
| Academic text | ~57.4% |

- Stemming produced broken tokens: `batteri`, `absolut`, `wa`
- Lemmatization preserved root meaning: `battery`, `absolute`, `be`
- Removing `almost` from "almost nobody likes spam" flips the meaning entirely

## Learning Outcomes

- Preprocessing choices are decisions, not defaults; the right approach depends on the task
- NLTK is lighter and faster; spaCy provides richer tagging out of the box
- Stemming follows blunt rules and produces unreadable output; lemmatization understands language
- Stop word removal needs context: intensity words and negations often carry meaning

## Files

- `L02_Robert_B_Thompson_ITAI_2373.ipynb` – Preprocessing lab notebook

## Dependencies

```
nltk
spacy
```

```bash
pip install nltk spacy
python -m spacy download en_core_web_sm
import nltk; nltk.download('punkt'); nltk.download('stopwords')
```

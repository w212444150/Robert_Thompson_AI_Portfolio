# L07 – Sentiment and Emotion Analysis

**Course:** ITAI 2373 | Houston Community College  
**Student:** Robert B. Thompson  
**Instructor:** Prof. Anna Deverakonda  
**Date:** May 2, 2026

---

## Problem Statement

Build a complete emotion detection system that works on both text and speech. Apply multiple sentiment analysis methods, compare their outputs, and extend the system to audio input.

## Approach

1. Applied VADER for rule-based polarity scoring on text
2. Applied TextBlob for polarity and subjectivity scores
3. Trained a logistic regression classifier on TF-IDF features for longer reviews
4. Extracted audio features (MFCCs, pitch, energy) using librosa for speech emotion classification

## Key Results

- VADER scored compound sentiment on a −1 to +1 scale without requiring training data
- TextBlob provided polarity and subjectivity scores efficiently on short text
- TF-IDF + logistic regression outperformed VADER on longer, structured reviews
- librosa extracted mel-frequency cepstral coefficients and pitch features from audio files for emotion classification

## Learning Outcomes

- VADER works best on social media and informal text with strong polarity signals
- TextBlob subjectivity scores add a dimension VADER does not provide
- ML classifiers on TF-IDF features generalize better when labeled training data is available
- Audio emotion analysis parallels text emotion analysis: both extract features, then classify

## Files

- `L07_Robert_Langdon_Thompson_Sentiment_Emotion_Analysis_.ipynb` – Lab notebook

## Dependencies

```
vaderSentiment
textblob
scikit-learn
pandas
numpy
matplotlib
seaborn
librosa
soundfile
```

```bash
pip install vaderSentiment textblob librosa soundfile
python -m textblob.download_corpora
```

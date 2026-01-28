# Image Processing & NLP: HMM Bigram POS Tagger

This repository contains the implementation of a Part-of-Speech (POS) tagger using a Bigram Hidden Markov Model (HMM). This project was developed as part of an Image Processing and Natural Language Processing curriculum.

## Project Overview
The project implements a sequence labeling system that assigns POS tags to words in a sentence. It utilizes the **Brown Corpus** from the NLTK library for training and evaluation.

### Key Features
- **HMM Bigram Model**: Implementation of transition and emission probabilities.
- **Viterbi Algorithm**: Dynamic programming approach for finding the most likely sequence of tags.
- **Smoothing Techniques**:
  - **Add-One (Laplace) Smoothing**: Handles zero probabilities for transitions and emissions.
  - **Pseudo-Word Smoothing**: Replaces low-frequency and unknown words with category-based pseudo-words (e.g., `fourDigitNum`, `allCaps`, `startsWithDollar`) to improve tagging accuracy for out-of-vocabulary words.
- **Error Analysis**: Detailed computation of error rates for known and unknown words, including confusion matrix generation.

## Requirements
The project requires the following Python libraries:
- `Pillow`
- `numpy`
- `matplotlib`
- `nltk`
- `tqdm`

You can install the dependencies using:
```bash
pip install -r requirements.txt
```

## Usage
Run the main script to train the model on the Brown Corpus and evaluate its performance:
```bash
python ex3.py
```

## Authors
- Malak Laham
- Zenab Waked

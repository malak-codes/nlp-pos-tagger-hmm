# HMM Bigram POS Tagger: Viterbi & Smoothing

This repository contains an implementation of a **Part-of-Speech (POS) Tagger** using a **Hidden Markov Model (HMM)** with a Bigram transition structure. The project focuses on statistical sequence labeling and handles the data sparsity problem using various smoothing techniques.

## Project Overview

The core objective of this project is to build a robust POS tagger that can accurately assign grammatical tags to words in a sentence. It utilizes the **Brown Corpus** for training and evaluation, implementing the **Viterbi Algorithm** for efficient decoding.

### Key Features

- **HMM Bigram Model**: Models the probability of a tag sequence based on the current word and the preceding tag.
- **Viterbi Algorithm**: A dynamic programming approach to find the most likely sequence of tags for a given sentence.
- **Smoothing Techniques**:
  - **Add-One (Laplace) Smoothing**: Handles zero-frequency transitions and emissions.
  - **Pseudo-Word Smoothing**: Replaces low-frequency and unknown words with category-based tokens (e.g., `initCap`, `containsDigit`) to improve generalization.
- **Error Analysis**: Includes a baseline comparison and detailed error reporting, including a confusion matrix for the most frequent tagging mistakes.

## Repository Structure

| File | Description |
| :--- | :--- |
| `ex3.py` | The main implementation script containing the `HMMBigram` class and evaluation logic. |
| `requirements.txt` | List of necessary Python dependencies (nltk, numpy). |
| `README.md` | Documentation providing an overview of the project and its components. |

## Requirements

The project requires the following Python libraries:
- `nltk`
- `numpy`

You can install the dependencies using:
```bash
pip install nltk numpy
```

## Usage

To run the POS tagger training and evaluation:
```bash
python ex3.py
```
The script will train the HMM model on the Brown Corpus, apply the Viterbi algorithm to the test set, and output the error rates and the most frequent tagging errors.

## Authors
- Malak
- Zenab

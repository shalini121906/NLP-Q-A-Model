# NLP-Q-A-Model
# Question Answering Model on the Stanford Question Answering Dataset (SQuAD)

## Overview

This repository contains code and resources for building a question-answering model using various Natural Language Processing (NLP) techniques, with a focus on the Stanford Question Answering Dataset (SQuAD).

## Dataset

The dataset comprises reading passages from Wikipedia articles, questions related to these articles, and corresponding answers. Each answer is a segment of text, or "span," from the reading passage.

## Preprocessing

### TextBlob

- The paragraph/context is segmented into multiple sentences.
- Each context is limited to a maximum of 10 sentences.

### Word2vec (GoogleNews)

- Sentence embeddings are generated for sentences from the context and questions.

## Training Model

The training data is prepared, and a multinomial logistic regression model is utilized for training. The achieved accuracy on the validation set is 65%.

## Results

An example context and question are provided to the model. The model predicts the correct index of the sentence in the context containing the answer to the given question.

### Example:

**Context:** "Mount Everest, also known as Sagarmatha in Nepal and Chomolungma in Tibet, is Earth's highest mountain above sea level, located in the Mahalangur Himal sub-range of the Himalayas. Its peak is 8,848.86 meters (29,031.7 feet) above sea level, making it one of the Seven Summits. The international border between China and Nepal runs across Everest’s precise summit point."

**Question:** "What is the height of Mount Everest above sea level?"

**Model Prediction:** [1]

**Predicted Answer:** "Its peak is 8,848.86 meters (29,031.7 feet) above sea level, making it one of the Seven Summits."


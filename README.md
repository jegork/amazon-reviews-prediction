# amazon-reviews-prediction

## Problem

The text of a review usually contains a lot of cues about the possible sentiment of a client about an item.
The goal of this project is to try to predict the rating of a review (on a scale from 1 to 5) based on the text of the review.

## Dataset

Data for this project was gathered by web scraping Amazon reviews from the list of the most popular items on [amazon.com](amazon.com).
Only the text and rating of the review were collected (thus, no personal data recorded).

## Methods

To approach the problem, two possible models will be used:
- LSTM model with precomputed word embeddings
- Cutting-edge transformer model

## Project structure

- [parse.ipynb](./parse.ipynb) scrapes Amazon using Selenium
- [amazon_reviews.csv](./amazon_reviews.csv) contains the scraped reviews in format [id, rating, text]

## Results

| Model | Training accuracy (%) | Test Accuracy (%) |
| --- | :---: | :---: |
| LSTM | 83 | 61 |
| Albert-base-v1 (implemented using TF) | 79 | 55 |
| Bert-base-uncased (implemeted using PyTorch) | 94 | 74 |


## Conclusions
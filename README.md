# Amazon Reviews Sentiment Analysis

This is a comprehensive approach to performing sentiment analysis on Amazon fine food reviews using two different techniques: VADER (a lexicon-based approach) and the RoBERTa Pretrained Model (a transformer-based approach). 

## Dataset
The dataset used in this sentiment analysis project is a collection 50K of Amazon fine food reviews. It includes various attributes such as the review's unique identifier (Id), the product identifier (ProductId), user identifier (UserId), the user's profile name (ProfileName), helpfulness scores (HelpfulnessNumerator and HelpfulnessDenominator), review score (Score), review time (Time), a summary of the review (Summary), and the full review text (Text).

## Workflow

## Step 0: Read in Data and NLTK Basics
Data Loading: You load the Amazon food review dataset and limit it to 500 reviews for analysis.
NLTK Setup: Download the necessary NLTK corpora and lexicons for text processing.

## Step 1: VADER Sentiment Scoring
VADER Analysis: Use the SentimentIntensityAnalyzer from NLTK to get sentiment scores (negative, neutral, positive, and compound) for each review using a Bag of Words approach.
Visualizations: Plot the VADER sentiment scores against the Amazon star ratings to understand the relationship between VADER scores and the reviews' actual ratings.

## Step 2: Roberta Pretrained Model
Model Setup: Use the AutoTokenizer and AutoModelForSequenceClassification from Hugging Face to load a pre-trained RoBERTa model.
Sentiment Analysis: Tokenize the reviews, pass them through the RoBERTa model, and use softmax to obtain sentiment probabilities (negative, neutral, positive).
Comparison: Compare VADER and RoBERTa results for the same review.

## Step 3: Combine and Compare Results
Data Aggregation: Combine the VADER and RoBERTa sentiment scores into a single DataFrame.
Visual Analysis: Use pair plots to visually compare the sentiment scores from both models across different star ratings.

## Step 4: Review Examples
Edge Cases: Analyze reviews where the star rating differs significantly from the sentiment scores provided by VADER and RoBERTa. This helps in identifying potential inconsistencies or biases in the models.

## Dependencies
- NumPy
- Pandas
- Matplotlib
- Seaborn
- NLTK (Natural Language Toolkit)
- Transformers (from Hugging Face)

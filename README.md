# Multi-class News Classification using BERT

Google Colab Link - https://colab.research.google.com/drive/1qoMCEMdapmS8xOFtzOF4Kpji2-1ETOzY#scrollTo=ZS6BqcXdInLy

## Introduction:
This project aims to perform multi-class classification on news articles from the BBC News dataset. The goal is to predict the category of each article from one of five categories: business, entertainment, politics, sport, and tech.

## Dataset:
The dataset contains news articles with their titles and categories. The distribution of categories is as follows:
- Sport: 505 articles
- Business: 503 articles
- Politics: 403 articles
- Entertainment: 369 articles
- Tech: 347 articles

## Preprocessing:
Before feeding the text data into the NLP model, various text cleaning functions are applied. These include converting text to lowercase, removing numbers, special characters, and stop words, lemmatizing words, and removing extra white spaces. These preprocessing steps are essential for improving the input data quality.

## Model Architecture:
The chosen model architecture is BERT (Bidirectional Encoder Representations from Transformers), a powerful pre-trained transformer-based language model. The model is fine-tuned using the BBC News dataset by adding a classification layer on top of the BERT model. During training, only the weights of the classification layer are updated, while the BERT model's weights are frozen. The model is trained for 5 epochs, and the best weights are saved using the EarlyStopping callback. In the second phase, the BERT layers are unfrozen, and the model is trained for additional epochs.

## Evaluation Metrics and Results:
The model's performance is evaluated using categorical cross-entropy loss and categorical accuracy metrics. The model achieves impressive results on the test set, with a test accuracy of 97.42% and a test loss of 0.1412. The precision, recall, and F1-score for each category are also calculated and reported in the classification report.

## Sample Predictions and Explanations:
After training the model, it can be used to predict the category of new text input. For example, when the text "Apple unveils new iPhone" is provided, the model predicts a high probability for the tech category, which is correct. This demonstrates the model's effectiveness in accurately classifying news articles based on their content.

## Possible Improvements:
While the model performs well, there are opportunities for further improvement:

1. Fine-tuning the model for more epochs or with a larger learning rate to optimize the model's weights further.
2. Experimenting with different pre-trained language models and architectures to see if they perform better on this task.
3. Augmenting the dataset with additional news articles to increase its size and diversity, which may enhance the model's ability to generalize to new data.

## Conclusion:
The BERT-based multi-class news classification model achieves high accuracy and performs well across all categories. With its robust performance, it accurately predicts the category of news articles based on their textual content, making it a valuable tool for automating news categorization tasks.

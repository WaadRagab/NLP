# Word Similarity Analysis using Fasttext 
## Project Overview
This project demonstrates the implementation of FastText Word Embedding for text data analysis. Using FastText, a word representation model developed by Facebook AI Research, the project focuses on training a model with a subset of the Yelp dataset, preprocessing the text, and extracting word similarities. 
The project explores both custom-trained FastText embeddings and pre-trained FastText models from Hugging Face to understand semantic relationships between words.

## Dataset
The dataset is the Yelp Academic Dataset, specifically the "tips" section containing user-generated reviews. The text data is extracted from the "text" column, and the first 50,000 lines are used for training the FastText model.

## Methodology
### Data Preprocessing
The text is preprocessed to remove unnecessary elements like punctuation and stopwords

### Custom FastText Model Training
A custom FastText model is trained on the preprocessed Yelp text data using Gensim's FastText implementation. 
The model parameters include:
  * Embedding Size: 300-dimensional word vectors.
  * Window Size: 5, for capturing the context of words within a 5-word window.
  * Min Word Count: 1, so all words that appear at least once are included.
  * Skip-gram: The model is trained using the skip-gram approach for word prediction.

### Pre-trained FastText Model
The project also integrates a pre-trained FastText model from Hugging Face, to demonstrate how pre-trained word embeddings can be used for semantic analysis.

### Word Similarity Analysis
The core functionality of the project is to calculate word similarities and nearest neighbors. The model is used to find:
* Most Similar Words: Identifies the top 10 words that are most similar to a given word.
* Negative Similarity: Identifies words that are least similar to a given word by analyzing negative context.

## Results
The FastText model successfully provides word similarities, both with the custom-trained model and the pre-trained model.

## Conclusion
This project highlights the power of FastText for learning word embeddings in Natural Language Processing (NLP) tasks. By comparing a custom-trained model on the Yelp dataset with a pre-trained model, we demonstrate the versatility of FastText in capturing word relationships, whether using small, domain-specific corpora or large, general-purpose embeddings.

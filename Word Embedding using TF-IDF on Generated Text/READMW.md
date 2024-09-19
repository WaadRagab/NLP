# TF-IDF on Generated Text
## Project Overview
This project demonstrates the implementation of a TF-IDF Vectorizer from scratch. The objective is to process and analyze text data by calculating the Term Frequency-Inverse Document Frequency (TF-IDF) for each word in a document corpus. 
The project utilizes text generation from GPT-2 to create sample documents, preprocesses the text, and computes the TF-IDF matrix to quantify the importance of each word within the corpus.

## Methodology
### Text Generation
Text samples are generated using GPT-2 for three topics: Olympics, Corona Virus, and Egypt Pyramids. The Hugging Face transformers library is used to generate short text snippets for these topics.

### Data Preprocessing
The text is preprocessed to remove unnecessary elements like punctuation and stopwords. Tokenization is applied to split the text into individual words.
Finally, a set of unique words is extracted for a concise representation of the processed text.

### TF-IDF Calculation
TF (Term Frequency): The number of occurrences of each word in a document.
IDF (Inverse Document Frequency): A measure of how rare a word is across the corpus.
TF-IDF Matrix: The product of TF and IDF, normalized to provide a meaningful representation of word importance across the documents.

## Results
The output of the project includes:
* TF-IDF Matrix: A matrix showing the TF-IDF values for each word in the corpus.
* Normalized TF-IDF Vectors: Document-specific TF-IDF vectors, normalized to help understand word importance relative to each document.

## Conclusion
This project provides an in-depth look at how text data can be transformed into numerical representations through the TF-IDF mechanism. The manual calculation of TF-IDF helps in understanding the core mechanics of the technique and its relevance in Natural Language Processing (NLP) tasks.

# Text Sequence Generation using RNN

## Project Overview
This project focuses on character and word-based text sequence generation using Recurrent Neural Networks (RNNs) and FastText embeddings. The project aims to predict the next character or word in a sequence from a Wikipedia article, showcasing the power of RNNs for language modeling and text generation.

## Dataset
The dataset is extracted from Wikipedia articles using the wikipedia Python library. For the demonstration, a search for "Spiderman" was conducted, and the article content was used as the training data for both character-level and word-level models.

## Methodology
### Data Preprocessing
* Character-Based Preprocessing: Each character in the article is tokenized and one-hot encoded for input to the RNN.
* Word-Based Preprocessing: Words are tokenized, cleaned, and converted into embeddings using pre-trained FastText word vectors.

### RNN Model
The model consists of:
Input layers for sequence data (character/word).
Several Simple RNN layers with 100 hidden units.
Dense layers with softmax activation for classification.
The model is trained to predict the next character or word in a sequence, with categorical cross-entropy as the loss function for character prediction and mean squared error for word embeddings.

### FastText Embeddings
For word-level predictions, FastText word embeddings are used to convert words into vector representations. The RNN model predicts the next word's embedding, which is then mapped back to a word using a nearest-neighbor search in the embedding space.

### Sequence Generation
Starting from a random sequence of characters, the RNN predicts the next character iteratively, generating new text.

## Model Training and Evaluation
* Character-based model: Achieved 98.42% accuracy after 50 epochs.
* Word-based model: Achieved 64.92% accuracy after 150 epochs.

## Conclusion
This project demonstrates the effectiveness of RNNs in sequence generation, both at the character and word level. By leveraging FastText embeddings for word-based modeling, we achieve meaningful word predictions and generate coherent text. The model architecture can be extended for various text generation tasks such as story completion or predictive text.

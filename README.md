# Predictive-Text-Generation-with-GRU-Model
This project uses a custom Gated Recurrent Unit (GRU) model for predictive text generation. 
While utilizing Google Colab for this project, I encountered a limitation due to high RAM usage which led to the session being closed prematurely. As a result, I was only able to train the model on a relatively small subset of the available dataset. I firmly believe that the model's performance would substantially improve if it were given the opportunity to train on a larger and more diverse dataset
The code is divided into several sections:

## Data Preparation
The data used in this project is a CSV file containing news articles. The data is loaded from a Google Drive link and then preprocessed. The preprocessing steps include:

* Extracting a subset of the data
* Converting all text to lowercase
* Tokenizing the text
* Removing non-English words
* Converting the tokenized text into sequences
* Padding the sequences to a fixed length
* Splitting the data into training and validation sets

## Feature Engineering
The tokenized and padded sequences of words are used as features for the model. The target is the next word in the sequence.

## GRU Implementation
A custom GRU model is implemented using TensorFlow. The GRU model consists of an embedding layer, a custom GRU layer, and a dense layer with a softmax activation function.

## Model Building
The model is compiled with the RMSprop optimizer and the categorical cross-entropy loss function. Early stopping and model checkpointing callbacks are used during training.

## Training and Evaluation
The model is trained on the prepared training data and evaluated on the validation data. The training process is monitored for the validation loss, and the model's weights are saved at the epoch with the lowest validation loss.

## Results Visualization
The code includes functions to predict the next word given an input text and to generate a sequence of text by repeatedly predicting the next word. These functions are used to demonstrate the model's predictive text generation capabilities.

## Usage
To use the model for text prediction, provide an input text to the predict_next_word function. To generate a sequence of text, provide an input text and the number of words to generate to the generate_text function.

## Potential Improvements
While the model performs reasonably well, there are several potential improvements that could be made:

* Use a larger part of the dataset
* Experiment with different model architectures or hyperparameters
* Use pre-trained word embeddings
* Implement a beam search or other advanced decoding method in the text generation function

## Conclusion
This project demonstrates how a custom GRU model can be used for predictive text generation. The model is capable of generating reasonably coherent and grammatically correct sentences, making it a good starting point for more advanced text generation tasks.

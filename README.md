
﻿# 06 Encoder Decoder

# Data
1. We load the tweet.csv file in dataframe explore the dataset


2. We clean the data and create the datasets with 70:30 train test split, and created the vocabs


# The Network / Model - Architecture

We have created as language model which is also a language model as it looks the entire sentence before predicting the sentiments.
below are the three classes-

1. Encoder : We have used LSTMCell here so that we can unroll the RNN word by word for a given tweet. We collect the output and stack them. The final hidden state and cell state are returned along with output


2. Decoder : Decoder takes the output from encoder as input along with last hidden and cell state as initial hidden and cell states. It runs for 1 step and its hidden state is fed to a Fully connected layer to give the output prediction vector.


3. Seq2Seq : It connects both encode and decoder and results the prediction vector


# The Network parameters

- Training hyperparameters
    - num_epochs = 10
    - learning_rate = 0.001
    - batch_size = 8

-  Model hyperparameters
    - input_size_encoder = len(TEXT.vocab)
    - input_size_decoder = 64 # Hidden dimention for output
    - output_size = len(LABEL.vocab)
    - encoder_embedding_size = 32
    - cell_state_size = 64
    - hidden_size = 64
    - num_layers = 1

# The training
Model achieves above 70% accuracy in less than 5 epochs
- Training Log



Epoch: 1
	Train Loss: 0.411 | Train Acc: 66.56%
	 Val. Loss: 0.243 |  Val. Acc: 72.36% 

Epoch: 2
	Train Loss: 0.333 | Train Acc: 66.56%
	 Val. Loss: 0.242 |  Val. Acc: 72.36% 

Epoch: 3
	Train Loss: 0.328 | Train Acc: 66.25%
	 Val. Loss: 0.242 |  Val. Acc: 72.36% 

Epoch: 4
	Train Loss: 0.291 | Train Acc: 66.56%
	 Val. Loss: 0.264 |  Val. Acc: 72.36% 

Epoch: 5
	Train Loss: 0.252 | Train Acc: 67.08%
	 Val. Loss: 0.251 |  Val. Acc: 72.36% 

Epoch: 6
	Train Loss: 0.185 | Train Acc: 69.27%
	 Val. Loss: 0.251 |  Val. Acc: 72.12% 

Epoch: 7
	Train Loss: 0.122 | Train Acc: 69.90%
	 Val. Loss: 0.413 |  Val. Acc: 67.31% 

Epoch: 8
	Train Loss: 0.079 | Train Acc: 71.35%
	 Val. Loss: 0.397 |  Val. Acc: 69.71% 

Epoch: 9
	Train Loss: 0.074 | Train Acc: 71.56%
	 Val. Loss: 0.322 |  Val. Acc: 72.36% 

Epoch: 10
	Train Loss: 0.060 | Train Acc: 72.08%
	 Val. Loss: 0.334 |  Val. Acc: 71.88% 

### Model results on manually / test dataset

1. We load the tweet.csv file in dataframe explore the dataset



2. We clean the data and create the datasets with 70:30 train test split, and created the vocabs


# The Network / Model - Architecture

We have created as language model which is also a language model as it looks the entire sentence before predicting the sentiments.
below are the three classes-

1. Encoder : We have used LSTMCell here so that we can unroll the RNN word by word for a given tweet. We collect the output and stack them. The final hidden state and cell state are returned along with output


2. Decoder : Decoder takes the output from encoder as input along with last hidden and cell state as initial hidden and cell states. It runs for 1 step and its hidden state is fed to a Fully connected layer to give the output prediction vector.


3. Seq2Seq : It connects both encode and decoder and results the prediction vector


# The Network parameters

- Training hyperparameters
    - num_epochs = 10
    - learning_rate = 0.001
    - batch_size = 8

-  Model hyperparameters
    - input_size_encoder = len(TEXT.vocab)
    - input_size_decoder = 64 # Hidden dimention for output
    - output_size = len(LABEL.vocab)
    - encoder_embedding_size = 32
    - cell_state_size = 64
    - hidden_size = 64
    - num_layers = 1

# The training
Model achieves above 70% accuracy in less than 5 epochs
- Training Log



Epoch: 1
	Train Loss: 0.411 | Train Acc: 66.56%
	 Val. Loss: 0.243 |  Val. Acc: 72.36% 

Epoch: 2
	Train Loss: 0.333 | Train Acc: 66.56%
	 Val. Loss: 0.242 |  Val. Acc: 72.36% 

Epoch: 3
	Train Loss: 0.328 | Train Acc: 66.25%
	 Val. Loss: 0.242 |  Val. Acc: 72.36% 

Epoch: 4
	Train Loss: 0.291 | Train Acc: 66.56%
	 Val. Loss: 0.264 |  Val. Acc: 72.36% 

Epoch: 5
	Train Loss: 0.252 | Train Acc: 67.08%
	 Val. Loss: 0.251 |  Val. Acc: 72.36% 

Epoch: 6
	Train Loss: 0.185 | Train Acc: 69.27%
	 Val. Loss: 0.251 |  Val. Acc: 72.12% 

Epoch: 7
	Train Loss: 0.122 | Train Acc: 69.90%
	 Val. Loss: 0.413 |  Val. Acc: 67.31% 

Epoch: 8
	Train Loss: 0.079 | Train Acc: 71.35%
	 Val. Loss: 0.397 |  Val. Acc: 69.71% 

Epoch: 9
	Train Loss: 0.074 | Train Acc: 71.56%
	 Val. Loss: 0.322 |  Val. Acc: 72.36% 

Epoch: 10
	Train Loss: 0.060 | Train Acc: 72.08%
	 Val. Loss: 0.334 |  Val. Acc: 71.88% 
     
     
 

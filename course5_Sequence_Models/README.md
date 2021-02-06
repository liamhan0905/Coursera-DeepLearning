### Key points from "Building a Recurrent Neural Network" project assignment (Week 1)

- Implemented a forward pass for the basic RNN and LSTM

### Key points from "Dinosaurus Island Character Level Language Model Final" project assignment (Week 1)

- Built a character level language model to generate new dinosaurus names.

### Key points from "Improvise a Jazz Solo with an LSTM Network" project assignment (Week 1)

- Implemented a model that uses an LSTM to generate music
- A sequence model can be used to generate musical values, which are then post-processed into midi music.
- Fairly similar models can be used to generate dinosaur names or to generate music, with the major difference being the input fed to the model.
- In Keras, sequence generation involves defining layers with shared weights, which are then repeated for the different time steps  1,…,Tx1,…,Tx .

### Key points from "Operations on word vectors" project assignment (Week 1)
- Used consine similiarity to find simliarity between words (e.g. 'father', 'mother' has similarity whereas 'monkey' 'laptop' does not)
- Used cosine simliarity to find analogy between words. (e.g. 'italy' -> 'italian :: 'spain' -> ?) The answer should be 'spanish'
- One-hot vectors do not do a good job of capturing the level of similarity between words (every one-hot vector has the same Euclidean distance from any other one-hot vector).
- Embedding vectors such as GloVe vectors provide much more useful information about the meaning of individual words
- Cosine similarity is a good way to compare the similarity between pairs of word vectors.
- Note that L2 (Euclidean) distance also works.
- For NLP applications, using a pre-trained set of word vectors is often a good way to get started.


### Key points from "Emojify" project assignment (Week 1)
- Using a baseline softmax model does well but it does not capture the relationship between words. But using the LSTM model resolves this issue.
- If you have an NLP task where the training set is small, using word embeddings can help your algorithm significantly.
- Word embeddings allow your model to work on words in the test set that may not even appear in the training set.
- Training sequence models in Keras (and in most other deep learning frameworks) requires a few important details:
- To use mini-batches, the sequences need to be padded so that all the examples in a mini-batch have the same length.
- An Embedding() layer can be initialized with pretrained values.
- These values can be either fixed or trained further on your dataset.
- If however your labeled dataset is small, it's usually not worth trying to train a large pre-trained set of embeddings.
- LSTM() has a flag called return_sequences to decide if you would like to return every hidden states or only the last one.
- You can use Dropout() right after LSTM() to regularize your network.
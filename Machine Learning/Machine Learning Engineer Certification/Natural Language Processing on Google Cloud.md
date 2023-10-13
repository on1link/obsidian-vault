#googleCloudPlatform 
# NLP on Google Cloud
## Quiz
* What are the options to create a processor for Document AI?
	* Create a custom processor and build it on your own.
	* Choose an existing processor created for a specialized task.
	* Choose an existing processor created for general purposes.
*  What are the three options provided by Google Cloud to develop an NLP project?
	* [[Pre-built API]]s, [[AutoML]], and custom training
* What is NOT an application of NLP?
	* Image Recognition 
* What are the three major components that the Dialogflow API hellps to identify in a conversation?
	* Intent (the topic), entity (the details), and context (the flow of the conversation)
# NLP with [[Vertex AI]]
## Quiz 
* What are the NLP tasks solved by [[AutoML]]?
	* Sentiment analysis
	* Text classification
	* Entity extraction
* What are the major stages of an end-to-end workflow to build an NLP project with [[Vertex AI]]?
	* Data preparation, model training, and model serving
* [[Vertex AI]] provides two solutions to build an NLP project. Which of the following is correct about these two solutions?
	* [[AutoML]], which is a no-code solution, and custom training, which is a code-based solution
# Text representation
## Quiz
* Which of the following is correct about [[one-hot encoding]] when you represent text with basic vectorization?
	* [[one-hot encoding#^60dc84 ]]
* What are the benefits of using word embedding (such as word2vec) compared to basic vectorization (such as one-hot encoding) when you convert text to vectors?
	* Compared to basic vectorization, which converts text to vectors without semantic meaning, word embeddings represents words in a vector space where the distance between them indicates semantic similarity and difference. 
	* You can use pre-trained word-embedding to represent text.
	* Compared to basic vectorization, which converts text to sparse vectors, word embedding converts text to dense vectors.
* Which of the following is NOT a major step of feature engineering in NLP?
	* Model Testing
* What is the difference between continuous bag-of-words (CBOW) and skip-gram, the two primary techniques of word2vec?
	* CBOW uses surrounding words to predict a center word, whereas skip-gram uses a center word to predict surrounding words.
# NLP models
## Quiz
* What is the key feature to enable a "memory" of an [[RNN]] (recurrent neural network)?
	* An RNN uses a mechanism called hidden state to carry the previous information to the next learning iteration.
* What is the coding in [[Keras]] to build the hidden layer of a [[GRU]] (gated recurrent unit) model?
	* GRU(units)
*  What are the major gates in a standard [[LSTM]] (long short-term memory) cell?
	* A standard [[LSTM]] cell includes three gates: the forget gate to forget irrelevant information, the input gate to remember relevant information, and the update gate to update new information.
# Advanced NLP models
## Quiz
* What is the problem that an encoder-decoder mainly solves?
	* [[Sequence-to-sequence]] problems such as machine translation where you translate sentences to another language.
*  Which of the following is correct about large language models?
	* Large in large language models refers to both huge training datasets and many parameters.
	* Large language models can be pre-trained for general purpose and then fine-tuned for specific tasks
	* [[Transformer]] and [[BERT]] are examples of large language models.
* What is the major improvement of [[BERT]] (Bidirectional Encoder Representations) compared to transformers?
	* [[BERT]] considers the order of the words in a sentence, whereas a transformer doesn't
	

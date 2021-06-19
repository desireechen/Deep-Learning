# Deep-Learning with TensorFlow

This is a collection of my own notes as I am learning more about Deep Learning. 

There is a mini-project using Keras on the Diabetes dataset. 

The other 3 notebooks using TensorFlow are created using Google Colab (I like their easy access to GPUs). 
There is 1 notebook each for Image Classification, Natural Language Processing and Time Series.  

### Image Classification

Data Preprocessing:

Use of `ImageDataGenerator` to generate batches of tensor image data with real-time data augmentation. Augmentation can take various forms such as a rescale, rotation, shift, shear, zoom, flip. Validation data should not be augmented. Only augment training data. Augmentation of training data helps the model to generalize better. 

Point the data generator to the directory (e.g. Train) that contains the sub-directories (e.g. A or B type of images). 

Training and evaluation:

Transfer Learning may be used. Here, `InceptionV3` which was pre-trained on the `ImageNet` dataset was used. Lock the pre-trained layers of the model and amend the last layer or the last few layers (can go further up the layers of the model). There are other transfer learning models suc as `VGG` and `ResNet` variants. 

Dropouts, which is a regularization technique, may be used. For binary classification problem, use `sigmoid` on the final output neuron. For multi-class classification, use `softmax`. There are other options of activation functions.

Model can be compiled using varous optimizers such as `RMSprop` or `Adam`. Choose appropriate loss function. For binary classification, one can choose `binary_crossentropy`. For multi-class, one can choose `categorical_crossentropy` or `sparse_categorical_crossentropy`. There are other options of loss functions.  

Callbacks may be used to stop training earlier if a certain metric value such as accuracy or loss is reached. 

### Natural Language Processing

Data Preprocessing:

Decide if stopwords need to be removed for the purposes of the particular analysis. Both sentences and labels need to be tokenized. When creating the Tokenizer, define the maximum number of words to keep (based on word frequency) and the handling of out-of-vocabulary tokens. Tokenizer does not care about punctuation and lower or upper cases of letters. 

Padding can be pre or post. If the padding is post and the sentence is shorter than the maximum length, the last words of the sentence will be padded. Maximum length ensures that all sentences are of the same length. 

Truncate can be pre or post. If the sentence is longer than the maximum length and truncate is pre, the beginning of the sentence will be removed.

Training and evaluation:

Global Vectors for Word Representation (GloVe) is an unsupervised learning algorithm for obtaining vector representations for words. GloVe contains various pre-trained word vectors such as 100 dimensions, uncased, 400K vocabulary. `embedding_dim` represents the number of dimensions that a word is projected onto. 

Recurrent Neural Network (RNN) suffers from short-term memory. In the case of NLP, short-term memory will result in words at the start of a sentence not having an effect at the end of a long sentence. To combat the issue of short-term memory, Gated Recurrent Unit (GRU) and Long Short-Term Memory (LSTM) are typically used in NLP. GRU is a type of RNN with size equals to the number of RNN units. LSTM can be either single-layer or multi-layers and can be Bi-directional or Uni-directional.

### Time Series and Sequences

To be filled up

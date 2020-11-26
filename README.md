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

To be filled up

### Time Series and Sequences

To be filled up

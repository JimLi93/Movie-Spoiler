# Movie-Spoiler

## Introduction

Build a RNN model to determine whether the given text contains a movie spoiler.

## Dataset

Use data provided on https://www.kaggle.com/datasets/rmisra/imdb-spoiler-dataset.

The dataset is collected from IMDB. It contains meta-data about items as well as user reviews with information regarding whether a review contains a spoiler or not.

Use 16917 samples from the reviews data.

### Data Prepocessing

* Convert text to lowercase
* Remove Punctuation
* Remove stop words<br>
Ex. "from", "all", etc. These words are required only for grammatical rules. <br>Use library `nltk.corpus.stopwords`.

### Model Layer

* Text Vectorization Layer
* Embedding Layer
* Bidirectional LSTM Layer

### Training Technique

* Adaptive Learning Rate<br>
Use `ReduceLROnPlateau` in `Keras.callbacks` to create an
adaptive learning rate as the loss begins to plateau.
* Early Stop<br>
Use `EarlyStopping` in `Keras.callbacks` to stop the training
process when additional training becomes unnecessary.

## Reference

https://asistdl.onlinelibrary.wiley.com/doi/full/10.1002/meet.14505001073

https://aclanthology.org/D14-1181.pdf

https://aclanthology.org/2021.eacl-main.315.pdf

https://www.kaggle.com/datasets/rmisra/imdb-spoiler-dataset

https://www.tensorflow.org/tutorials/keras/text_classification

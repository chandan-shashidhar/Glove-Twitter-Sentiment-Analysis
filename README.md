# Twitter Sentiment Analysis

## Overview
This package will perform sentiment analysis on tweets or similar short texts.
Pre-trained word embeddings from GloVe are used as a frozen 
input to Keras, afterwhich a CNN learns and predicts on the classification.

## Requirements
```
* keras
* sklearn
* numpy
```

## Usage

1. Download the GloVe embedings for twitter, unzip into a /glove directory.
        
        wget http://nlp.stanford.edu/data/glove.twitter.27B.zip
        
2. Download the twitter sentiment data set into / directory.

        wget http://thinknook.com/wp-content/uploads/2012/09/Sentiment-Analysis-Dataset.zip

3. Run *[Optional since model.h5 and weights.h5 have been provided]* 

        python train.py

    Which will create a model.h5 and weights.h5 files.
4. Run 

        echo "This is a sample tweet to predict on" | python predict.py
    Or
        
        cat file-containing-one-tweet-per-line.txt | python predict.py
        

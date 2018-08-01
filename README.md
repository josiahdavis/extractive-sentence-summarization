# Extractive sentence summarization

In this notebook I provide a python class for creating a full-sentence summary of document. Sentence summary is useful for document summary applications where it is beneficial to give users a quick sense of what is contained in the document to determine if they wanted to read further. There are two different categories of text summarization techniques: extractive and abstractive. Extractive techniques generally require less data, are unsupervised, and "extract" sentences from the document. Conversly, abstrative techniques require labeled training data, are supervised, and create summaries made up of generated, rather than extracted sentences. Methods, which are implemented in the open source package sumy, are all extractive and include KL-sum, Edmundson, LexRank, LSA, and random.

## Packages

Package versions are:

```
sumy==0.7.0
nltk==3.2.5
```

## Usage

To clone this notebook:

`git clone https://github.com/josiahdavis/extractive-sentence-summarization.git`

To run a simple example, please refer to the notebook in the repository.


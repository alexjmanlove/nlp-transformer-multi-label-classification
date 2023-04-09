# Transformer for NLP Multi-Label Classification
One of the most iconic and influential machine learning papers of all time [Attention is All You Need (2019)](https://arxiv.org/abs/1706.03762) introduced the transformer architecture for sequence to sequence modelling.

This GitHub repo explores the use of the transformer architecture with an Encoder-only design for the task of multi-label classification. In the .ipynb we build an Encoder-only model in TensorFlow to classify movie genres given their English description text. 

The main advantage of using an Encoder-only transformer model for multi-label classification as opposed to recurrent neural networks or LSTMs is that Transformers can process variable-length input sequences and capture long-range dependencies without suffering from vanishing/exploding gradients. This makes Transformers particularly useful for natural language processing tasks such as text classification. 

## Test Set Evaluation

### Confusion Matrices
![image](https://user-images.githubusercontent.com/79708390/230681669-9ff6507a-9842-4fc7-a20c-294a87d2316c.png)

### Performance Metrics
![image](https://user-images.githubusercontent.com/79708390/230681654-d9d698e0-64c4-45af-b25a-07fb3b472156.png)

### Examples

![samples](https://user-images.githubusercontent.com/79708390/230747732-d8e16b50-9590-400d-a6d8-b768b622c9f7.png)

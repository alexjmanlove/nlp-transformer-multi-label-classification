# Transformer for Multi-Label Classification
One of the most iconic and influential machine learning papers of all time [Attention is All You Need (2019)](https://arxiv.org/abs/1706.03762) introduced the transformer architecture for sequence to sequence modelling.

This GitHub repo explores the use of the transformer architecture with an Encoder-only design for the task of multi-label classification. In the .ipynb we build an Encoder-only model in TensorFlow to classify movie genres given their English description text. 

The main advantage of using an Encoder-only transformer model for multi-label classification as opposed to recurrent neural networks or LSTMs is that Transformers can process variable-length input sequences and capture long-range dependencies without suffering from vanishing/exploding gradients. This makes Transformers particularly useful for natural language processing tasks such as text classification. 


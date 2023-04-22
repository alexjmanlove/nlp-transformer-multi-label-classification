# Transformer for NLP Multi-Label Classification
One of the most iconic and influential machine learning papers of all time [Attention is All You Need (2019)](https://arxiv.org/abs/1706.03762) introduced the transformer architecture for sequence to sequence modelling.

This GitHub repo explores the use of the transformer architecture with an Encoder-only design for the task of multi-label classification. In the .ipynb we build an Encoder-only model in TensorFlow to classify movie genres given their English description text. 

The main advantage of using an Encoder-only transformer model for multi-label classification as opposed to recurrent neural networks or LSTMs is that Transformers can process variable-length input sequences and capture long-range dependencies without suffering from vanishing/exploding gradients. This makes Transformers particularly useful for natural language processing tasks such as text classification. 

There is a severe class imbalance in the data. For this reason it is important to consider not only the accuracy but also other metrics such as precision and recall. 


## Test Set Evaluation

### Confusion Matrices
![image](https://user-images.githubusercontent.com/79708390/233810521-e88918da-0e73-4f47-85f5-0fc9f2760cf4.png)

As we can see the model has struggled to learn the features which properly distinguish the minority classes, and in particular failed to make any test predictions for Fantasy, History and Mystery. 

### Performance Metrics
![image](https://user-images.githubusercontent.com/79708390/233810513-96aad71a-193a-4eb7-8ee7-259a939e3fa0.png)


### Examples

> `description = A team of scientists unlock the secrets of teleportation and unleash an infinite universe of possibilities. Now they must face an unprecedented threat   in a race against time to save humanity from catastrophe.`        
    `prediction = [('Science Fiction', 0.8753725), ('Action', 0.5229177)]` 


> `description = A mute orphan overcomes devastating adversity and learns to speak again in this tragic coming-of-age story.`     
    `prediction = [('Drama', 0.9552138)]`


>`description = Experience the brutal intensity of D-Day like never before, as recolored footage offers a unique perspective of the heroic soldiers storming the beaches of Normandy.`     
    `prediction = [('Documentary', 0.86815417)]` 


>`description = The streets erupt in a symphony of chaos as an FBI agent, framed for a murder she didn't commit, fights tooth and nail against a corrupt system to clear her name and take down those who betrayed her.`     
    `prediction = [('Action', 0.79605836), ('Thriller', 0.70161915)]` 


>`description = Get ready for a night of non-stop chuckles as three bumbling clowns unwittingly find themselves center stage in a circus act, causing chaos to ensue at every turn!`     
    `prediction = [('Comedy', 0.98350406)]` 


>`description = Embark on a fascinating journey into the hidden world of nocturnal mammals, as this captivating nature programme delves deep into their unique life cycle, behaviors, and survival strategies under the veil of darkness.`    
    `prediction = [('Documentary', 0.9015226)]` 


>`description = Join a mischievous group of kids on an enchanted quest through a mystical realm, as they rally together to thwart the evil wizards and rescue the elf kingdom.`    
    `prediction = [('Animation', 0.70773137), ('Family', 0.5901838), ('Adventure', 0.572934)]`


>`description = Amid the ruins of a once-thriving city, a lone survivor must navigate a harrowing, post-apocalyptic wasteland plagued by a deadly virus and the worst of human nature, in a desperate struggle to survive.`    
    `prediction = [('Horror', 0.7364862)]`


>`description = A robot assassin from a dystopian future is sent back in time to kill the leader of the human resistance.`    
    `prediction = [('Science Fiction', 0.9042124), ('Action', 0.7169777)]` 

# Named Entity Recognition Using Spacy

**In this notebook, I'm using Spacy library to tag the named enities with a focus on locations and addresses.
Working with Spacy is pretty easy and give us a very quick results to tackle this problem with a reasonable accuracy. Actually this part took less than one hour. All the remaining time was to tackle the problem using recurrent neural network models (Bi-directional LSTM with pretrained embedding layer).**

I tried to work in a different direction by building a deep sequence model using bi-directional LSTM and I found a very good paper that worked on a similar problem. This paper introduced an approach to achieve a very good results in named entity recognition problems.  This model achieved F1 score of 91.62 on CoNLL-2003 and 86.28 on OntoNotes. You can find this paper here https://arxiv.org/abs/1511.08308

I used this BI-LSTM model and I tried to fine-tune its hyperparameters and train the model for only 10 epochs (I don't have GPUs on my machine), I got results about 83% for F1 score on the training set and abut 82% on the test set. This direction really needs more time to get better results by apply cross validation on the hyperparameters to pick the best values and retrain the model. It's worthy to metion that that model has a pre-trained embedding layer (Glove) with embedding vectors of deminsion (50,) per each word and this layer in the proposed model is set as non-trainable layer. I will share these LSTM trials later in another notebook to make things better organized.  

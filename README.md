``` 
    Name     : Choudhary Vikashkumar S
    Roll no. : 19075025
    Dept.    : CSE(B.Tech)
```


# **Lab-Task-3** :
Implement Word Embedding through **Word2Vec** (Glove and Skipgram) and **GloVe** Embeddings .<br>
And Visulisation plots (PCA and t-SNE) for most similar words as well as the complete embedding space.

>* In very simplistic terms, Word Embeddings are the texts converted into numbers and there may be different numerical representations of the same text.Word embedding is one of the most popular representation of document vocabulary. It is capable of capturing context of a word in a document, semantic and syntactic similarity, relation with other words, etc.
>* Word2Vec is a method to construct such an embedding. It can be obtained using two methods (both involving Neural Networks): Skip Gram and Common Bag Of Words (CBOW)
<br>Training data is from **English** language.<br>

**Files Pattern in this repo :**
1. **Word2Vec_CBOW Embedding**
   * word2vec_cbow_.ipynb {code Implemented file }
   * model 
2. Word2Vec_Skipgram Embedding
   * word2vec_skipgram_.ipynb
   * model
3. Glove Embedding 
   * glove.ipynb
   * model
4. Spelling Error Detection using CNN
   * CNN.ipynb
   * model
> ##  Word2Vec CBOW :
```
This method takes the context of each word as the input and tries to predict the word corresponding to the context.
The CBOW model tries to understand the context of the words and takes this as input. It then tries to predict words 
that are contextually accurate. Let us consider an example for understanding this. Consider the sentence: ‘It is a 
pleasant day’ and the word ‘pleasant’ goes as input to the neural network. We are trying to predict the word ‘day’ here.

```

> ## Word2Vec Skip-gram :
```
The skip-gram neural network model is actually surprisingly simple in its most basic form; I think it’s all of the 
little tweaks and enhancements that start to clutter the explanation.

Chunking is an important part of NLP because it works as the prerequisite 
for :
  * Named Entity Recognition

We have only one item for framing the features , that is the "word" column and second "POS" column.
```


> ## GloVe :
```
GloVe is an unsupervised learning algorithm for obtaining vector representations for words. Training is performed 
on aggregated global word-word co-occurrence statistics from a corpus, and the resulting representations showcase 
interesting linear substructures of the word vector space. 
Training
The GloVe model is trained on the non-zero entries of a global word-word co-occurrence matrix, which tabulates how 
frequently words co-occur with one another in a given corpus. Populating this matrix requires a single pass through 
the entire corpus to collect the statistics. For large corpora, this pass can be computationally expensive, but it
is a one-time up-front cost. Subsequent training iterations are much faster because the number of non-zero matrix 
entries is typically much smaller than the total number of words in the corpus. 

Commands
1. git clone https://github.com/stanfordnlp/glove
2. cd glove && make
3. ./GolVe.sh
```


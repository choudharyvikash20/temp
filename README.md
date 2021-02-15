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
```
1. Word2Vec_CBOW Embedding
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
   
   All the plots (PCA and T-SNE and present in the notebook of every subtasks )
```
This task is also submited on G-drive https://drive.google.com/drive/folders/1SKoeN7PLtiFRbVTRUNdGbKEtpcsIjX_-?usp=sharing so large size models is submit of G-drive

> ##  Word2Vec CBOW(Continuous Bag of words):
```
This method takes the context of each word as the input and tries to predict the word corresponding to the context.
The CBOW model tries to understand the context of the words and takes this as input. It then tries to predict words 
that are contextually accurate. Let us consider an example for understanding this. Consider the sentence: ‘It is a 
pleasant day’ and the word ‘pleasant’ goes as input to the neural network. We are trying to predict the word ‘day’ here.

Getting top 5 similar to this {place, computer, hero, time , game} words according to model created.
Output :
- model
- plot using PCA and T-SNE of whole data
- plot of 
```

> ## Word2Vec Skip-gram :
```
The main idea behind the Skip-Gram model is this: it takes every word in a large corpora (we will call it the focus 
word) and also takes one-by-one the words that surround it within a defined ‘window’ to then feed a neural network 
that after training will predict the probability for each word to actually appear in the window around the focus 
word.

Getting top 5 similar to this {place, computer, hero, time , game} words according to model created.
Output :
- model
- plot using PCA and T-SNE of whole data
- plot of 
```


> ## GloVe :
```
GloVe is an unsupervised learning algorithm for obtaining vector representations for words. Training is performed 
on aggregated global word-word co-occurrence statistics from a corpus, and the resulting representations showcase 
interesting linear substructures of the word vector space. 

The GloVe model is trained on the non-zero entries of a global word-word co-occurrence matrix, which tabulates how 
frequently words co-occur with one another in a given corpus. Populating this matrix requires a single pass through 
the entire corpus to collect the statistics. For large corpora, this pass can be computationally expensive, but it
is a one-time up-front cost. Subsequent training iterations are much faster because the number of non-zero matrix 
entries is typically much smaller than the total number of words in the corpus. 

Getting top 5 similar to this {place, computer, hero, time , game} words according to model created.
Output :
- model
- plot using PCA and T-SNE of whole data
- plot of 

Commands to install toolkit
1. git clone https://github.com/stanfordnlp/glove
2. cd glove
3. make
```
> ## Spelling Error Detection using CNN(Convolutional Neural Networks) :
```
It is an interaction of identification and of mistakenly spelled words in a content. In common language, it 
fundamentally examines the content and concentrates contained in it. It at that point looks at each word to a 
rundown of effectively spelled words (a greater amount of like a word reference) and henceforth distinguishes
the incorrectly spelled words.

Usage - We have actualized a binary characterization model of CNN in which we have utilized a dataset which 
contains accurately spelled words alongside some wrongly spelled words in the proportion of 10:1 (i.e., 10 
right words for each wrongly spelled word).

At that point we have passed the embeddings of this dataset shaped into the neural organization which repeat 
through different ages where every age has a specific exactness and misfortune esteem which is adjusted after 
each age to build the precision of the yield model.

Finally we have a trained CNN model with accuracy of 91.363639 %
```

``` 
    Name     : Choudhary Vikashkumar S
    Roll no. : 19075025
    Dept.    : CSE(B.Tech)
```


# **Lab-Task-4** :

- **Recurrent Neural Network (RNN)** allows you to model memory units to persist data and model short term dependencies. It is also used in time-series forecasting for the identification of data correlations and patterns. It also helps to produce predictive results for sequential data by delivering similar behavior as a human brain.
-A **Bidirectional LSTM**, or biLSTM, is a sequence processing model that consists of two LSTMs: one taking the input in a forward direction, and the other in a backwards direction. BiLSTMs effectively increase the amount of information available to the network, improving the context available to the algorithm (e.g. knowing what words immediately follow and precede a word in a sentence).

**Files Pattern in this repo :**

1. **Chunking**
   - **RNN**
      - Chunking_using_RNN.ipynb
      - Chunking_using_RNN_model.pb
   - **Bi-LSTM** (contain 2 files)
2. Named Entity Recognition
   - **RNN** (contain 2 files)
   - **Bi-LSTM** (contain 2 files)
3. Part-Of-Speech tagging
   - **RNN** (contain 2 files)
   - **Bi-LSTM** (contain 2 files)

> ## Major steps followed in all the sub-tasks:
```
- Data Preparation (Downloading data using NLTK tool kit or Importing from device  i.e. conll2000 and conll2003 )
- Data separation  (separate the words from the tags)
- Data Spliting    (split the data in training and testing data and use the train_test_split function from Scikit-Learn)
- Convert the word dataset to integer dataset, both the words and the tags.
- Padding 
- Create the Architecture for our RNN/Bi-LSTM model
- Training model
- Accuracy calculation
- Visualization using graph
- Example
```

> ## Part-Of-Speech(POS) tagging :
```
Part-of-Speech (POS) tagging, it may be defined as the process of converting a sentence in the form 
of a list of words, into a list of tuples. Here, the tuples are in the form of (word, tag). We can 
also call POS tagging a process of assigning one of the parts of speech to the given word.

POS tagging is an important part of NLP because it works as the prerequisite 
for :
  * Chunking
  * Named Entity Recognition

The dataset is extracted from the provided CoNLL shared task 2000.

```
 
|  | **Accuracy on test data of POS Tagging** |
|------ |---------|
| RNN | 97.63493537902832 % |
| Bi-LSTM | 98.25547337532043 % |


> ## Chunking :
```
Chunking, one of the important processes in natural language processing, is used to identify parts 
of speech (POS) and short phrases. In other simple words, with chunking, we can get the structure 
of the sentence. It is also called partial parsing.

Chunking is an important part of NLP because it works as the prerequisite 
for :
  * Named Entity Recognition

```

|  | **Accuracy on test data of Chunking** |
|------ |---------|
| RNN | 97.0231831073761 % |
| Bi-LSTM | 97.39433526992798 % |

> ## Named Entity Recognition :
```
Named entities are phrases that contain the names of persons, organizations, locations, times and 
quantities.

The dataset is extracted from the provided CoNLL NER shared task 2003
```
|  | **Accuracy on test data of Named Entity Recognition(NER)** |
|------ |---------|
| RNN | 99.89232420921326 % |
| Bi-LSTM | 99.50173497200012 % |

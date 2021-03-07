``` 
    Name     : Choudhary Vikashkumar S
    Roll no. : 19075025
    Dept.    : CSE(B.Tech)
```


# **Lab-Task-4** :




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

> ## Part-Of-Speech(POS) tagging :
```
Part-of-Speech (POS) tagging, it may be defined as the process of converting a sentence in the form 
of a list of words, into a list of tuples. Here, the tuples are in the form of (word, tag). We can 
also call POS tagging a process of assigning one of the parts of speech to the given word.

POS tagging is an important part of NLP because it works as the prerequisite 
for :
  * Chunking
  * Named Entity Recognition

We have only one item for framing the features , that is the "word" column.

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

We have only one item for framing the features , that is the "word" column and second "POS" column.
```

|  | **Accuracy on test data of Chunking** |
|------ |---------|
| RNN | 93.24988918673618 % |
| Bi-LSTM | 92.84040779281085 % |

> ## Named Entity Recognition :
```
Named entities are phrases that contain the names of persons, organizations, locations, times and 
quantities.

We have only one item for framing the features , that is the "word" column ,second "POS" column and 
third "Chunking" column.

The dataset is extracted from the provided CoNLL NER shared task 2003
```
|  | **Accuracy on test data of Named Entity Recognition(NER)** |
|------ |---------|
| RNN | 93.24988918673618 % |
| Bi-LSTM | 92.84040779281085 % |

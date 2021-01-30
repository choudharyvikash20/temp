``` 
    Name     : Choudhary Vikashkumar S
    Roll no. : 19075025
    Dept.    : CSE(B.Tech)
```


# **Lab-Task-2** :



For this task I have used CRF++ tool for training and Testing.<br>
**English language** data is used.<br>
Training and Testing are used in Conll format.<br>
* Command used for traning is : ``` crf_learn template train_data model```<br>
Here the **template** is the file which contains features, on which the model is created. And **train_data** is the file containig the training data in Conll format

* Command used for testing is : ``` crf_test -m model test_data```<br>

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


```
|  | **Accuracy** |
|------ |---------|
| POS_template_1 | 93.24988918673618 % |
| POS_template_2 | 92.84040779281085 % |
| POS_template_3 | 93.29421449226417 % |

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
|  | **Accuracy** |
|------ |---------|
| Chunking_template_1 | 96.05082635033877 % |
| Chunking_template_2 | 95.94740063744011 % |
| Chunking_template_3 | 93.96753699052283 % |

> ## Named Entity Recognition :
```
Named entities are phrases that contain the names of persons, organizations, locations, times and 
quantities.

We have only one item for framing the features , that is the "word" column ,second "POS" column and 
third "Chunking" column.
```

|  | **Accuracy** |
|------ |---------|
| NER_template_1 | 96.68075536081275 % |
| NER_template_2 | 96.81065570592114 % |
| NER_template_3 | 96.71953158323316 % |

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
Above the **model** is the model created through the training and **test_data** contains the test data.

**Result** file contains Accuracy,Precision, Recall the F-measure.

**Files Pattern in this repo :**
1. **Chunking**
   - **chunking_1**
      - chunking_template-1
      - chunking_model-1
      - chunking_output-1
      - chunking_result-1
   - chunking_2 (Contains 4 files)
   - chunking_3 (Contains 4 files)
2. Named Entity Recognition
   - NER_1 (Contains 4 files)
   - NER_2 (Contains 4 files)
   - NER_3 (Contains 4 files)
3. Part-Of-Speech tagging
   - POS_1 (Contains 4 files)
   - POS_2 (Contains 4 files)
   - POS_3 (Contains 4 files)

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
**Template 1:** (Total contains 7 features )<br>
 Used a default template containing :<br>5("token-feature") and<br> 2 ("bigram-feature") .<br><br>
**Template 2:** (Total contains 6 features )<br>
 Reduced the feature set of the default template to :<br> 3 ("token-features"),<br>2 ("bigram-feature") and <br> 1("trigram-feature") <br><br>
**Template 3:**<br>
 It contains only 3 ("token-feature") .<br>
 
 
|  | **Accuracy** | |
|------ |---------|-|
| POS_template_1 | 93.24988918673618 % | This default template contains some complex features that leads to Overfitting the training data.|
| POS_template_2 | 92.84040779281085 % | Some important features were removed due too which accuracy decreses. |
| POS_template_3 | 93.64037402114950 % | Contains only few features which were good for this task which leads to increase the accuracy.|

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
**Template 1:** (Total contains 19 features )<br>
 Used default template as provided by the CoNLL shared task 2000.<br>
 This contains : <br>10 ("token-feature")<br>
                 6  ("bigram-feature")<br>
                 3  ("trigram-feature")<br><br>
**Template 2:** (Total contains 19 features )<br>
  Changed some of the features from default template.<br>
  This contains : <br>10 ("token-feature")<br>
                 3  ("bigram-feature")<br>
                 3  ("trigram-feature")<br>
                 3  (more complex features)<br><br>
**Template 3:**(Total contains 2 features )<br>
 This template is very simple, which contains only two basic features.<br><br>
 
 
|  | **Accuracy** | |
|------ |---------|-|
| Chunking_template_1 | 96.05082635033877 % | Used default template from Conll task which gives best accuracy. |
| Chunking_template_2 | 95.94740063744011 % | Some features were removed , due to which accuracy decresed. |
| Chunking_template_3 | 93.96753699052283 % | This contains only 2 features which are not sufficient for good result. |

> ## Named Entity Recognition :
```
Named entities are phrases that contain the names of persons, organizations, locations, times and 
quantities.

We have only one item for framing the features , that is the "word" column ,second "POS" column and 
third "Chunking" column.

The dataset is extracted from the provided CoNLL NER shared task 2003
```
**Template 1:** (Total contains 32 features )<br>
 Used default template as provided in the CRF++ Example for NER.<br>
 This contains : <br>15 ("token-feature")<br>
                 11  ("bigram-feature")<br>
                 6  ("trigram-feature")<br><br>
**Template 2:** (Total contains 21 features )<br>
  Many features are removed from default template.<br>
  This contains : <br>13 ("token-feature")<br>
                 8  ("bigram-feature")<br>
                 
**Template 3:**(Total contains 13 features )<br>
 Some more features are removed from default template.<br>
  This contains : <br>9 ("token-feature")<br>
                 4  ("bigram-feature")<br>

|  | **Accuracy** | |
|------ |---------|-|
|NER_template_1|96.68075536081275 % | Used default template from CRF++ example which was for language japanes.|
|NER_template_2|96.81065570592114 % | Removed some complex features , due to which overfitting decresed and accuracy some what incresed |
|NER_template_3|96.71953158323316 % | Some more features were removed |

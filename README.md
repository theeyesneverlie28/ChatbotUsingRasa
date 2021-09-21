# PROJECT : Auto-learning of Chatbot

## Project objective
The objective of this project is auto-learning of Chatbot from manuals.

In our case, we have to extract tables from manuals (with Problem and following Cause-Solution),
then create a model that predicts the suitable cause-solution for problems asked by users.

To do so, we will first have to complete a state of the art on this subject. Once this study has
been carried out, we will have to implement the tool.

Furthermore, we would like to make the process of Chatbot automatic rather than modify the
code each time we run it. Hence, we decided to realise this project.
## Tutorial
We have created in this Git a directory named "input" containing the raw manual with its edited version and 2 files containing communication intents and actions. The "output" directory contains the Rasa files.

There are 3 code files:

- "full_code" contains everything we tried.

- "final_code" is the file that we recommend to execute.

- "paraphrase" is the file to make paraphrases.
## Input
In this part, we read the manual pdf file on python and restructure the data in this file. The input
is a manual of a BAUKNECHT washing machine.

## Methods
### Restructure data
#### Read a pdf file
We had to use specific packages to read tables from a pdf file. By our researches, the packages
most applied are Camelot and Tabulat.
#### Restructure the data
When using the Camelot package, it led to 4 tables as a result. This happened because the
Camelot package only reads table by table, page by page. We needed one whole table so we had
to merge them.
### Paraphrasing
Paraphrasing is a phase with goals to repeat something written or spoken using different words,
that remains the meaning.
#### Training Algorithm-T5 (4)
T5 is a new transformer model from Google that is trained in an end-to-end manner
with text as input and modified text as output.
#### Google translate
We can do the paraphrase with Google translate. The idea is that from a sentence in English,
we translate it into another language (for example French) and rewrite it in English, so we get a
paraphrase of this sentence.
### Create Rasa files
## Results
### Test
We prepared a conversation tests file containing 12 examples to check the accuracy of trained
model.

We verified that combining two algorithms increased the accuracy of Chatbot. However, it required
a lot of time on training model.
### Demo
We had a short demo of conversation with Chatbot. It returned the corresponding cause-solution
for each problem entered. The conmmunication was quite interactive due to the intents like
greeting, goobye or affirm,etc.. 

## References
[1]R.  Boscacci,BART  for  Paraphrasing  with  Simple  Transformers.https://towardsdatascience.com/bart-for-paraphrasing-with-simple-transformers-7c9ea3dfdd8c.

[2]R. Goutham,Paraphrase any question with T5 (Text-To-Text Transfer Transformer)— Pretrained model and training script provided.https://towardsdatascience.com/paraphrase-any-question-with-t5-text-to-text-transfer-transformer-pretrained-model-and-cbb9e35f1555.

[3]Kristof,paraphrasing   via   google   translate.https://pypi.org/project/paraphrase-googletranslate/.

[4]M. S. Z. RIZVI,Learn how to Build and Deploy a Chatbot in Minutes using Rasa.https://www.analyticsvidhya.com/blog/2019/04/learn-build-chatbot-rasa-nlp-ipl/.

[5]A. Roberts,Exploring Transfer Learning with T5: the Text-To-Text Transfer Transformer.https://ai.googleblog.com/2020/02/exploring-transfer-learning-with-t5.html.

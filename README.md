# Understanding Siri - NLP Model powered by BERT

***Project***

In this project, I developed a neural network using BERT, Google's cutting-edge language model, to perform both sentence-level intent classification and Named Entity Recognition with ~99% accuracy.

***Context***

I worked on this project as part of the Advanced Cohort of the Inspirit AI program.

***References/Collaborators***

**References**

Here are the links to the Google Collab notebooks:

N1: https://colab.research.google.com/drive/1M53rP5NKSTO1xx-6zC8AKlJfXwidxBs9?usp=sharing

N2: https://colab.research.google.com/drive/1TAt5SJ441WCT3UZn03Zzqn_zU6T7YQaB?usp=sharing

N3: https://colab.research.google.com/drive/1o3ODS3RTd5yvaN6-L8d_2mNpVotqb3qr?usp=sharing


Here are some resources that I looked through out of curiosity to understand the inner workings of BERT:

The Illustrated Transformer:
https://jalammar.github.io/illustrated-transformer/

Original Paper (Transformer Architecture):
Attention Is All You Need -
https://arxiv.org/pdf/1706.03762.pdf

Multi-Head Attention:
https://becominghuman.ai/multi-head-attention-f2cfb4060e9c

Visualizing A Neural Machine Translation Model (Mechanics of Seq2seq Models With Attention):
https://jalammar.github.io/visualizing-neural-machine-translation-mechanics-of-seq2seq-models-with-attention/


All other references (e.g. to data sources) are included within the text and code cells.

**Collaborators**

My mentor was a Stanford graduate in CS, who provided advice and information on certain technical aspects of BERT and general NLP theory and techniques. 

Throughout this project, I analyzed verbal commands to mimic the capabilities of digital assistants such as Siri in two ways:

a) predicting the *intent* of the speaker

and

b) extracting interesting *named entities* within the command.

For clarification, Part (b) is known as **Named Entity Recognition** (NER), which locates and classifies entities in text into pre-defined categories such as person names, organizations, and locations.

Part (a) is a sentence-level classification task, and part (b) - or NER - is a token-level classification task.

## Example
Here is an example of the format of the final predictions that I produced:

The command "Book a table for two at Le Ritz for Friday night" becomes the following JSON output:

```
{
    'intent': 'BookRestaurant',
    'slots': {
        'party_size_number': 'two',
        'restaurant_name': 'Le Ritz',
        'timeRange': 'Friday night'
    }
}
```

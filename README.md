# Text Summarization

## Overview
Text summarization is a challenging task in the field of natural language processing, aimed at condensing the content of a given text while retaining its most important information. The system takes a longer document or article as input and generates a concise and coherent summary, making it ideal for various applications such as information retrieval, content generation, and document summarization. This project focuses on implementing and/or finetuning language models using neural networks. It aims to assess the quality of text summarization generated by our neural network models using human evaluation. 

While automated metrics like ROUGE are valuable, they may not capture the nuanced aspects of summary coherence, fluency, and relevance. Human evaluation provides a more comprehensive understanding of the quality of generated summaries.

[Amazon Fine Food Reviews](https://www.kaggle.com/datasets/snap/amazon-fine-food-reviews) was used as our dataset for all models. Due to computational constraints, only around 70000 reviews were used for training and testing.


## Contents
A total of 4 variations of models were implemented/fine-tuned
1. LSTM
2. LSTM with W2V embeddings
3. BART
4. T5

Based on human evaluation of coherence, conciseness, and relevance, T5 model achieved the greatest accuracy in capturing the essence of the source text. Below is an actual summary from our fine-tuned T5 model:

```
input_text = 'the  toy  seems  pretty  durable  which  is  a big  winner  for  me  because  usually  the  toys  that  i buy  for  my  dogs  do  not  last  quite  long the  toy  itself  has  a tennis  ball  inside  which  i really  like  you  do  not  have  to  buy  two  separate  toys i  also  love  the  fact  that  it  has  a ball  inside  and  they  can  try  to  entertain  themselves so  awesome'

output_summary = 'love the fact that it comes with ball'
```

## Installation
```
pip install nltk py7zr datasets torch torchvision torchaudio rouge.score sentencepiece
pip install accelerate transformers -U
``` 

## Usage
Run notebooks as per linked
Final summaries are stored in [Summaries](https://github.com/cheekychy/Text-Summariser/blob/main/summaries.md)

## Motivation
I chose to proceed with text summarization using Deep Learning was to understand Neural Networks a little more. Along the way, I also picked up new knowledge on the different types of NNs availble, like bidrectional LSTM models and Transformers, as well as coming across various language models like BERT and T5. This was my first exposure to Deep Learning, and it has definitely made me consider going into this field in the future. 

## Todo
Create a web application to showcase the final fine-tuned model with custom queries 

## Credits
This little project could not have been possible without the help of my mentor, Teck Wu! Special thanks to the Girls In Tech (GIT) team for organizing this summer programme for us tech girlies. :-)

Special thanks to [Analytics Vidhya](https://www.analyticsvidhya.com/blog/2019/06/comprehensive-guide-text-summarization-using-deep-learning-python/), [Hugging Face](https://huggingface.co/) for inspiration code snippets for aiding me along in this journey.

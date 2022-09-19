# What is Paraphrasing?
Paraphrasing is the act of writing some text using different words, phrases, and sentence structures without changing its meaning. Paraphrasing is an important technique utilized in writing
Artificial intelligence is used to automate the process of paraphrasing. There exist many paraphrase tools that can paraphrase text automatically. However, programmers can also directly create a Python program to paraphrase text.
In this project we are going to check out both methods of paraphrasing, a) by using Python, and b) by using paraphrasing tools.
# How To Paraphrase Your Text Using Python?
There are are plenty of different ways to create a paraphrasing program using Python. However, currently one of the most popular methods is to use transformers.

**Transformers** are artificial neural networks that are able to learn the context of a text. This means they can understand its meaning. This makes them ideal to use for paraphrasing as you can count on them to not butcher the meaning of the text.

In this project we will be using the Pegasus model. It is a transformer that uses an encode-decoder model for sequence-to-sequence learning. You can learn more about the Pegasus model by reading its documentation.

Pegasus stands for “Pre-training with Extracted Gap-Sentences for Abstractive Summarization”. Don’t be confused by this. Abstractive summaries are basically paraphrasing as well. An abstract summary summarizes a text by rewriting all of its main points in a concise form using different wording. 

Now that we have covered the basics, let’s see how we can use Pegasus for paraphrasing.
# Import dependencies
``` 
!pip install sentence-splitter
!pip install transformers
!pip install SentencePiece 
```
# Setting Up Pegasus 
The next thing we need to do is to import the Pegasus model and set it up because we need it to do the paraphrasing. Without it, things will become more difficult.
To  set up Pegasus, we need to install Pytorch first. Pytorch is a Python package that provides high-level features of tensor computation and deep neural networks. It is the underlying framework that powers Pegasus.
``` 
  import torch
  from typing import List
  from transformers import PegasusForConditionalGeneration, PegasusTokenizer 
  model_name = 'tuner007/pegasus_paraphrase' 
  torch_device = 'cuda' if torch.cuda.is_available() else 'cpu'
  tokenizer = PegasusTokenizer.from_pretrained(model_name)
  model = PegasusForConditionalGeneration.from_pretrained(model_name).to(torch_device)
``` 
Running this code should download a bunch of files that look like this. The Pytorch model bin is a pretty large file, so don’t worry if it takes a bit of time to download it.

![image](https://github.com/inesgh1/Paraphrasing-Web-App/blob/main/set_peagasus.png)

# Test the model


















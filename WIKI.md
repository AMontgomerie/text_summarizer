# Details

This was built using Python, Flask, PyTorch, and Huggingface Transformers. 

## Model
The text summarization model is DistilBart which is a distilled version of BART. [BART](https://arxiv.org/abs/1910.13461) is a slightly modified version of BERT with a bidirectional encoder and left-to-right decoder. The left-to-right decoder improves performance on autoregressive text generation tasks (such as summarization). "Distilled" here refers to [the method proposed in this paper](https://arxiv.org/abs/1910.01108) which claims to reduce model size by 40% while retaining 97% of performance.

I used [a pretrained implementation of DistilBart](https://huggingface.co/sshleifer/distilbart-cnn-6-6) and its tokenizer from Huggingface.

# Issues
Although I used a distilled version of the model, it's still fairly large and so takes some time to load the first time a user attempts to summarize a text.

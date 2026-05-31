# Transformer from Scratch: English to Hindi Translator 🚀

Hey there! Welcome to my project where I built a Transformer model entirely from scratch using PyTorch. 

If you've ever wanted to look under the hood of how modern AI language models work, this is a great place to start. Instead of relying on pre-built libraries like HuggingFace that abstract away all the math, I wanted to build the actual architecture described in the famous *"Attention Is All You Need"* paper, block by block.

## What's inside?

This repository contains everything you need to train and run an English to Hindi language translation model:

- `transformer_scratch.py`: The heart of the project. This is where you'll find the raw PyTorch implementation of the Transformer. It includes the Encoder, Decoder, Multi-Head Attention blocks, Positional Encodings, and Feed-Forward layers—all built from the ground up.
- `train.ipynb`: A Jupyter Notebook walking you through the training process. 
- `inference.ipynb`: A notebook to test out the trained model and see it translate English sentences into Hindi.

## Why did I build this?

Honestly? To learn. It's one thing to import a model and use `.generate()`, but it's a completely different beast to write the matrix multiplications and attention mechanisms yourself. I wanted to deeply understand how information flows through the Self-Attention mechanisms and the Encoder-Decoder attention layers. By focusing on an English to Hindi translation task, I was able to test the model on a real-world, complex sequence-to-sequence problem.

## Getting Started

1. **Clone the repo:**
   ```bash
   git clone <your-repo-url>
   cd "Language Translator"
   ```

2. **Check out the code:**
   I highly recommend opening `transformer_scratch.py` first. I've broken down the classes (like `MultiHeadAttentionBlock` and `EncoderBlock`) to make it as readable and understandable as possible.

3. **Train it yourself:**
   Fire up `train.ipynb` and follow along to train the model on the English-Hindi dataset. Note: Training from scratch takes a good amount of computing power, so a GPU is highly recommended!

4. **Run some translations:**
   Once you have a `model.pt` saved, open up `inference.ipynb` to try out your own translations. 

## Stuff to note

- The trained model weights (`model.pt`) and `__pycache__` directories are deliberately ignored in Git because they are huge/unnecessary. You'll generate your own weights during training!
- The dataset used for English-Hindi translation needs to be pre-processed before training (as seen in the notebooks). 

Feel free to fork this, play around with the hyperparameters, or use it as a learning resource to build your own Transformers. If you spot any bugs or have suggestions, pull requests are always welcome!

Happy coding! ✨

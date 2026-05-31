# Transformer from Scratch: English to Hindi Translation

This repository contains a complete, ground-up implementation of the original Transformer architecture described in the paper *"Attention Is All You Need"* (Vaswani et al., 2017), built entirely in PyTorch. 

The primary objective of this project is to develop a deep, practical understanding of modern sequence-to-sequence language models. By avoiding high-level abstractions provided by libraries like HuggingFace, this project manually constructs the core mathematical and structural components of the network. The resulting model is configured and trained specifically for English-to-Hindi translation.

## Architecture Highlights

The core logic of the model is implemented directly from the paper's specifications. Key components include:

- **Attention Mechanisms**: Custom implementations of scaled dot-product attention and multi-head attention blocks.
- **Encoder-Decoder Stacks**: Full implementation of both the encoder and decoder layers, including the cross-attention mechanisms necessary for sequence generation.
- **Positional Encodings**: Manual calculation of sine and cosine positional embeddings to inject sequence order information into the input embeddings.
- **Feed-Forward Networks**: Position-wise feed-forward networks implemented within each residual attention block.

## Project Structure

- `transformer_scratch.py`: The core architectural implementation. This file contains all custom PyTorch `nn.Module` classes (e.g., `EncoderBlock`, `MultiHeadAttentionBlock`, `LayerNormalization`).
- `train.ipynb`: A comprehensive training pipeline, covering dataset preprocessing, tokenization, and the training loop required to optimize the model on English-Hindi translation pairs.
- `inference.ipynb`: An evaluation notebook demonstrating how to load trained weights and perform inference to translate new English sentences into Hindi.

## Getting Started

1. **Clone the repository:**
   ```bash
   git clone https://github.com/adkdev200-ops/English-to-Hindi--Transformer-from-scratch-.git
   cd "Language Translator"
   ```

2. **Explore the Implementation:**
   I recommend reviewing `transformer_scratch.py` first to see how the mathematical formulations from the paper translate into PyTorch tensors and matrix operations.

3. **Training the Model:**
   To train the model locally, follow the steps in `train.ipynb`. Please note that training a Transformer architecture from scratch is computationally intensive; a CUDA-enabled GPU is strongly advised.

4. **Running Inference:**
   Once training is complete, use `inference.ipynb` to load your generated `model.pt` weights and execute translations.

## Technical Notes

- **Model Weights**: The trained model weights (`model.pt`) and local Python cache files (`__pycache__`) are excluded from version control to maintain a clean and lightweight repository. You will generate your own model weights locally during the training pipeline.
- **Data Preparation**: The raw text data requires preprocessing and tokenization using the logic provided in the notebooks before it can be processed by the model.

Feel free to use this repository as a technical reference for your own learning, or fork it to experiment with architectural modifications.

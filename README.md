# DocGPT (A Decoder-Only Implementation of GPT's Architecture)

This project implements the GPT2 (Generative Pre-trained Transformer) architecture. The model is specifically designed as a decoder-only variant. It has been trained on a dataset comprised of physiology books(approx 11M tokens). This project is an understanding of Andrej Karpathy's Neural Network series.

## Project Overview

The project consists of two primary parts:

### 1. Bigram Model

This section aims to introduce the basic implementation of the Bigram probabilistic model. It serves as a fundamental step to understanding attention mechanisms.

### 2. DocGPT Notebook

The notebook named "DocGPT" forms the core of the project. Initially, the dataset comprised approximately 10 million characters extracted from physiology books. The data has undergone preprocessing, and an architecture encompassing liner layer, softmax, multi-head attention, feed-forward layers, residual connections, and dropout has been developed.

The layer ordering within this architecture is inspired by the "Attention Is All You Need" paper, defining the Transformer architecture. This implementation focuses solely on a decoder-based language model to simplify the complexity of implementation.

## Training Metrics and Results

### Training Metrics

<img width="392" alt="Screenshot 2023-11-22 at 23 22 26" src="https://github.com/JeethuSrini/Doctor-GPT/assets/85613102/76b7b209-02d2-47ac-b790-056621ef8317">

Final Results: train loss 1.1304, val loss 1.4530

### Generations Output

<img width="598" alt="sample" src="https://github.com/JeethuSrini/Doctor-GPT/assets/85613102/f65f29d0-9072-43ba-9f37-5bf79561c99d">

## Note on Generations

It's important to note that the generations produced by the model are currently random. The model has not undergone fine-tuning specifically for question-answering tasks.

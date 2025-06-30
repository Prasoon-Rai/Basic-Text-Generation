# 🧠 Basic Text Generation using RNN

This project demonstrates a character-level text generation model built using Recurrent Neural Networks (RNNs) in TensorFlow/Keras. It is intended as a learning experiment and may not produce coherent or meaningful output — the primary goal is to understand the core ideas behind sequence modeling.

## 📘 What This Notebook Does

The notebook walks through the full process of building a basic text generator:

### 1. **Text Preprocessing**
- Loads a short text string as the dataset.
- Maps each character to a unique integer.
- Splits the text into sequences to predict the next character.
- One-hot encodes input sequences.

### 2. **Model Construction**
The model is built using `keras.Sequential` and includes:
- A `GRU` layer (or simple RNN)
- A `Dense` output layer with softmax activation

### 🔧 Model Architecture

```
Input (sequence of characters)
    ↓
One-Hot Encoding
    ↓
GRU / SimpleRNN Layer (units=128)
    ↓
Dense Layer (units = total unique characters, activation='softmax')
    ↓
Output (next predicted character)
```

> This model learns to predict the next character in a sequence based on context from previous characters.

### 3. **Training**
- Trains using sparse categorical crossentropy.
- Optimized with Adam.
- Training is minimal and focused on the process, not performance.

### 4. **Text Generation**
- Takes a single character as a seed.
- Predicts one character at a time iteratively to build a sequence.

## 🎯 Purpose

This notebook is for educational purposes:
- Learn the basics of RNN-based text generation
- Understand character-level tokenization and sequence modeling
- Gain hands-on experience with sequence-to-one prediction

> ⚠️ **Disclaimer**: This model is not meant for production use. It was trained on a tiny dataset with few epochs and will not generate meaningful text.

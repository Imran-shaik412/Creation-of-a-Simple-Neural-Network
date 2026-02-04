# Creation-of-a-Simple-Neural-Network
# Simple PyTorch Neural Network

This repository contains a minimal PyTorch example demonstrating how to define a basic feedforward neural network using `torch.nn.Sequential`.

## 📄 File Overview

### `copy_of_day3fn.py`

This script defines a small neural network model with the following structure:

* **Input layer:** 2 features
* **Hidden layer:** 4 neurons with ReLU activation
* **Output layer:** 1 neuron

The model is suitable for learning simple regression or binary classification tasks (with an appropriate loss function).

## 🧠 Model Architecture

```text
Input (2) → Linear(2, 4) → ReLU → Linear(4, 1) → Output (1)
```

## 🧪 Code Snippet

```python
import torch
import torch.nn as nn

model = nn.Sequential(
    nn.Linear(2, 4),
    nn.ReLU(),
    nn.Linear(4, 1)
)
```

## 🚀 Requirements

* Python 3.x
* PyTorch

Install PyTorch by following the official instructions at:
[https://pytorch.org/get-started/locally/](https://pytorch.org/get-started/locally/)

## ▶️ Usage

You can import the model into a training script and pair it with:

* A loss function (e.g., `nn.MSELoss`, `nn.BCEWithLogitsLoss`)
* An optimizer (e.g., `torch.optim.SGD`, `torch.optim.Adam`)

Example:

```python
criterion = nn.MSELoss()
optimizer = torch.optim.Adam(model.parameters(), lr=0.001)
```

## 📝 Notes

* This file was originally generated from a Google Colab notebook.
* The model definition is intentionally simple for learning and experimentation purposes.

## 📚 Learning Context

This project appears to be part of a learning or practice session focused on understanding neural network basics in PyTorch.

---

Feel free to extend this model with more layers, different activation functions, or training logic!

# Backpropagation From Scratch — Numpy-Only (Jupyter Notebook)

This repository contains a single Jupyter notebook that implements a **feed-forward neural network** and trains it using **gradient descent with backpropagation**, written entirely with **NumPy** (no TensorFlow/PyTorch). It’s intended as an educational, fully transparent walk-through of the math and the code.

---

## What’s inside

* Step-by-step sections:

  1. Setup and data preparation
  2. Network architecture definition
  3. Forward propagation
  4. Backpropagation (manual gradients)
  5. Training loop (gradient descent)
  6. Evaluation and visualization
* Clean, modular functions for network operations and gradients (e.g., `network_function`, `cost`, and Jacobians like `J_W1`, `J_b1`, `J_W2`, `J_b2`, `J_W3`, `J_b3`).
* Lightweight, framework-free code you can adapt for experiments.

---

## Requirements

* Python 3.8+
* NumPy
* Matplotlib


## Key functions (at a glance)

* `network_function(x)` → returns layer activations up to the output
* `cost(x, y)` → mean squared error (MSE) style objective used in the notebook
* `reset_network()` → re-initializes parameters
* Gradient/Jacobian helpers used in backprop:

  * `J_W1(x, y)`, `J_b1(x, y)`
  * `J_W2(x, y)`, `J_b2(x, y)`
  * `J_W3(x, y)`, `J_b3(x, y)`

These expose the math of backprop explicitly, step by step.

---

## How the training loop works (conceptually)

1. **Forward pass**: compute activations layer by layer.
2. **Loss**: compare predictions to `y` with a differentiable cost function.
3. **Backward pass**: compute gradients for each parameter group (`W1/b1`, `W2/b2`, `W3/b3`) using the chain rule.
4. **Update**: subtract a scaled gradient (learning rate × gradient) from each parameter.
5. **Repeat** for several epochs/iterations until convergence.



This notebook is an educational rewrite showing backpropagation in detail, built only with NumPy and Matplotlib.


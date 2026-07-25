# CS3807 — Deep Learning Laboratory
## Lab 2: Implementation of a Multi-Layer Perceptron for Multi-Class Image Classification

This experiment implements a Multi-Layer Perceptron using TensorFlow/Keras to classify grayscale clothing images into 10 categories. It covers the full deep learning workflow — image preprocessing, model construction, training, evaluation, and automated hyperparameter optimization using RandomizedSearchCV.

A baseline MLP (784 → Dense(128, ReLU) → Dense(64, ReLU) → Dense(10, Softmax)) is trained first, followed by a hyperparameter search over layer count, neuron width, learning rate, batch size, optimizer, activation function, and dropout rate. The best configuration found is retrained and compared against the baseline.

## Dataset

**Fashion-MNIST** — 60,000 training images and 10,000 test images across 10 clothing categories, each a 28×28 grayscale image.

## Repository Contents

- `Source Code.ipynb` — Colab notebook with all tasks - dataset exploration, preprocessing, model building, training, evaluation, and hyperparameter search.
- `Additional Tasks.ipynb` - Colab note book with code for XOR gate using MLP.
- `Lab 2 - Multilayer Perceptron.pdf` — Full lab report in PDF (theory, procedure, results, plots with inferences, discussion, conclusion).
- `figures/` — Generated plots (sample images, class distribution, accuracy/loss curves, confusion matrix, hyperparameter search results) as PNGs.

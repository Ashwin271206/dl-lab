# CS3807 — Deep Learning Laboratory
## Lab 3: Implementation of Convolutional Neural Networks (CNNs) for Image Classification

This experiment implements a Convolutional Neural Network using TensorFlow/Keras to classify color images into 10 categories. It covers the full deep learning workflow — convolution and pooling fundamentals, feature map visualization, hyperparameter (kernel size, stride, padding) analysis, model construction, training, and evaluation.

A CNN following the architecture Input → Conv → ReLU → MaxPool → Conv → ReLU → MaxPool → Flatten → Dense → Softmax is trained using the Adam optimizer for 20 epochs. Additional exercises cover manual output-size and parameter calculations, ReLU vs Sigmoid activation comparison, Max Pooling vs Average Pooling comparison, and the effect of increasing convolutional filter count.

## Dataset

**CIFAR-10** — 50,000 training images and 10,000 test images across 10 object categories, each a 32×32 RGB image.

Dataset source: [https://www.kaggle.com/datasets/pankrzysiu/cifar10-python](https://www.kaggle.com/datasets/pankrzysiu/cifar10-python)

## Repository Contents

- `Source Code.ipynb` — Colab notebook with all tasks - dataset exploration, convolution and pooling experiments, feature map visualization, model building, training, evaluation, and additional exercises.
- `Lab 3 - Convolutional Neural Networks.pdf` — Full lab report in PDF (theory, procedure, results, plots with inferences, discussion, conclusion).
- `figures/` — Generated plots (sample images, class distribution, kernel/stride/padding comparisons, feature maps, accuracy/loss curves, confusion matrix) as PNGs.

## How to Run

The experiments are designed to run directly in **Google Colab**.

1. Open / upload the `Source Code.ipynb` notebook in [Google Colab](https://colab.research.google.com/).
2. For better performance, go to **Runtime → Change runtime type** and select **GPU** as the hardware accelerator.
3. Provide your Kaggle API key (`kaggle.json` file) to the Colab Runtime.
4. Run all cells using **Runtime → Run all**.
5. The notebook will automatically perform dataset exploration, convolution/pooling experiments, model training, evaluation, and generate the required plots and results.

No local Python environment or additional setup is required.
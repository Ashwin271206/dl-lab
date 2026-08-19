# CS3807 — Deep Learning Laboratory
## Lab 4 : Comparative Study of Deep Convolutional Neural Network Architectures Using Transfer Learning

This experiment compares five deep convolutional neural networks - LeNet5, AlexNet, VGG16, GoogleNet (InceptionV3) and ResNet50 classify color images into 10 categories using transfer learning for the pretrained architectures. It covers the full deep learning workflow — convolution and pooling fundamentals, feature map visualization, hyperparameter (kernel size, stride, padding) analysis, model construction, training, and evaluation.

Pretrained architecture were used, and last blocks were unfrozen and finetuned for VGG16, GoogleNet and ResNet50, while AlexNet and LeNet5 were trained from scratch. A further hyperparameter study was done among few configurations, and was optimized. Omptimizers like Adam and SGD were compared, and metrics of frozen layers and finetuned layers were also compared. 

## Dataset

**CIFAR-10** — 50,000 training images and 10,000 test images across 10 object categories, each a 32×32 RGB image.

Dataset source: [https://www.kaggle.com/datasets/pankrzysiu/cifar10-python](https://www.kaggle.com/datasets/pankrzysiu/cifar10-python)

## Repository Contents

- `Source Code.ipynb` — Colab notebook with all tasks - dataset exploration, convolution and pooling experiments, feature map visualization, model building, training, evaluation, and additional exercises.
- `Lab 4 - Transfer Learning.pdf` — Full lab report in PDF (theory, procedure, results, plots with inferences, discussion, conclusion).
- `outputs/` — Generated plots (sample images, class distribution, kernel/stride/padding comparisons, feature maps, accuracy/loss curves, confusion matrix) as PNGs, and result table CSVs.

## How to Run

The experiments are designed to run directly in **Google Colab**.

1. Open / upload the `Source Code.ipynb` notebook in [Google Colab](https://colab.research.google.com/).
2. For better performance, go to **Runtime → Change runtime type** and select **GPU** as the hardware accelerator.
3. Provide your Kaggle API key (`kaggle.json` file) to the Colab Runtime.
4. Run all cells using **Runtime → Run all**.
5. The notebook will automatically perform dataset exploration, convolution/pooling experiments, model training, evaluation, and generate the required plots and results.

No local Python environment or additional setup is required.
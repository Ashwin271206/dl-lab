# CS3807 - Deep Learning Laboratory

**Shiv Nadar University Chennai**  

**Degree & Branch:** B.Tech Artificial Intelligence & Data Science  

**Semester:** V  

**Subject Code & Name:** CS3807 – Deep Learning Laboratory  
 
**Name:** Ashwin S  

**Reg. No:** 24011101007  

**Class:** AI-DS 'A'  

---

## About this Repository

This is the master repository for all lab experiments completed as part of the CS3807 Deep Learning Laboratory course. Each experiment is organized into its own folder, containing the code, report, and generated outputs for that experiment.

## Structure

```
.
├── Lab 1/         # Single-Layer Perceptron
├── Lab 2/         # Multi-Layer Perceptron
├── Lab 3/         # Convolutional Neural Networks
├── Lab 4/         # Transfer Learning (CNN Architectures)
├── Lab 5/         # CNN Training, Regularization & Tuning
├── Lab 6/         # RNN, LSTM & GRU
├── Lab 7/         # Autoencoders & VAEs
├── ...
└── README.md
```

Each experiment folder is self-contained and includes:

- **Code** – Google Colab / Kaggle notebook with the full implementation.
- **Dataset** – Dataset used, or instructions on how it is loaded.
- **Report** – LaTeX & PDF report documenting objective, theory, methodology, results, and analysis.
- **Images** – Generated plots and figures.
- **Results** – Metrics, logs, and comparison tables from training and evaluation.

Refer to the README within each experiment folder for details specific to that experiment.

## Experiments

### Lab 1 - Single-Layer Perceptron

A manual, NumPy-based implementation of the perceptron learning algorithm. It is applied to classify banknotes as authentic or forged using the Bank Note Authentication dataset, and separately to learn the AND, OR, and NOT logic gates, visualizing the decision boundary and weight updates at every training step. Results are also compared against Scikit-learn's Perceptron implementation.

### Lab 2 - Multi-Layer Perceptron

An MLP built with TensorFlow/Keras to classify Fashion-MNIST clothing images into 10 categories. A baseline dense network is trained first, followed by a hyperparameter search (layer count, width, learning rate, batch size, optimizer, activation, dropout) via RandomizedSearchCV, with the best configuration compared against the baseline. An additional notebook covers the XOR problem using an MLP.

### Lab 3 - Convolutional Neural Networks

A CNN built with TensorFlow/Keras to classify CIFAR-10 images into 10 categories. The experiment covers convolution and pooling fundamentals, feature map visualization, and the effect of kernel size, stride, and padding, alongside comparisons of ReLU vs. Sigmoid activations, max vs. average pooling, and varying filter counts.

### Lab 4 - Transfer Learning (CNN Architectures)

A comparative study of five architectures - LeNet5, AlexNet, VGG16, GoogleNet (InceptionV3), and ResNet50 - on CIFAR-10. Pretrained VGG16, GoogleNet, and ResNet50 are fine-tuned by unfreezing their final blocks, while LeNet5 and AlexNet are trained from scratch. Adam and SGD optimizers, along with frozen vs. fine-tuned layer performance, are compared across a hyperparameter study.

### Lab 5 - CNN Training, Regularization & Tuning

A comprehensive study of the CNN training pipeline using a pretrained MobileNetV2 on the Oxford-IIIT Pet dataset (37 cat/dog breeds). It covers weight initialization schemes (Zero, Random, Xavier, He), regularization (L2, Dropout, Batch Normalization), optimizers (SGD, Momentum, RMSProp, Adam), hyperparameter tuning, feature-extraction vs. fine-tuning transfer learning, and 5-fold cross-validation to select the best configuration.

### Lab 6 - RNN, LSTM & GRU

An end-to-end study of sequence learning using Vanilla RNN, LSTM, and GRU architectures on the UCI Human Activity Recognition (HAR) dataset, covering BPTT and vanishing/exploding gradients, and comparing the three models on accuracy, F1-score, parameter count, and training time across different sequence lengths. It also extends to video understanding on UCF101 using a MobileNetV2 feature extractor with an LSTM/GRU, and a synthetic sequence-to-sequence reversal task with an encoder-decoder.

### Lab 7 - Autoencoders & VAEs

A study of representation learning and generative modeling on MNIST using a Fully Connected Autoencoder, a Convolutional Autoencoder, a Denoising Convolutional Autoencoder, and a Variational Autoencoder. The experiment evaluates reconstruction quality (MSE, MAE, SSIM) across latent dimensions and noise levels, and uses the VAE's 2D latent space to visualize the learned distribution, generate new digits, and interpolate between digit classes.

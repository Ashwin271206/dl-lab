# CS3807 — Deep Learning Laboratory
## Lab 7 : End-to-End Study of Autoencoders, Convolutional Autoencoders, Denoising Autoencoders and Variational Autoencoders

This experiment studies the complete deep learning workflow for image representation, reconstruction, denoising and generative modeling using Autoencoders and their variants. It covers the encoder–latent–decoder structure, reconstruction-based learning, controlled noise injection, reconstruction evaluation, the probabilistic latent representation of Variational Autoencoders, the reparameterization trick, and comparison of deterministic and variational latent representations.

The primary task uses the MNIST Handwritten Digit dataset. Images of shape 28×28×1 are normalized to [0,1] and used, without labels, as both the input and the reconstruction target. The experiment trains and compares a Fully Connected Autoencoder, a Convolutional Autoencoder, a Denoising Convolutional Autoencoder and a Variational Autoencoder using the same experimental conditions, and evaluates them using MSE, MAE, SSIM, parameter count and training time.

The experiment also studies the effect of latent dimension on reconstruction quality using dimensions of 2, 8, 16 and 32, and the effect of noise level using Gaussian noise (σ = 0.1, 0.2, 0.3) and salt-and-pepper noise. For the Variational Autoencoder, a 2-dimensional latent space is used to visualize the learned latent distribution, generate new digit images by sampling from the prior, and perform latent-space interpolation between digit classes.

## Dataset

- **MNIST Handwritten Digit** dataset contains grayscale images of handwritten digits from 0 to 9, each of spatial dimension 28×28×1. A recommended laboratory subset of 10,000 training images and 2,000 test images is used.
Dataset Source: [https://www.kaggle.com/datasets/hojjatk/mnist-dataset](https://www.kaggle.com/datasets/hojjatk/mnist-dataset)

## Repository Contents

- `Source Code.ipynb` — Kaggle notebook with all tasks - dataset loading, fully connected autoencoder, convolutional autoencoder, denoising autoencoder, variational autoencoder, model building, training, evaluation, and additional exercises.
- `LaTeX Code.tex` — Full lab report in LaTeX (theory, procedure, results, plots with inferences, discussion, conclusion).
- `figures/` — Generated plots (reconstructions, training/validation loss curves, noise-level comparisons, latent-space visualization, generated samples, interpolation grids, error distribution) as PNGs, and result table CSVs.

## How to Run

The experiments are designed to run directly in **Kaggle**.

1. Open / upload the `Source Code.ipynb` notebook in [Kaggle](https://www.kaggle.com/).
2. For better performance, go to **Settings → Accelerator** and select **GPU T4 x2** as the hardware accelerator.
3. Add the MNIST dataset (`hojjatk/mnist-dataset`) from Kaggle into the input.
4. Run all cells using **Run All**.
5. The notebook will automatically perform all mentioned tasks and generate the required plots and results.

No local Python environment or additional setup is required.
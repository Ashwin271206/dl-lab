# CS3807 — Deep Learning Laboratory
## Lab 5 : Comprehensive Study of CNN Training, Regularization, Optimization, Hyperparameter Tuning, Transfer Learning and Cross-Validation  

This experiment studies the complete deep learning workflow for image classification using the MobileNetV2 convolutional neural network on the Oxford-IIIT Pet dataset, which contains 37 categories of cat and dog breeds. It covers weight initialization, regularization and overfitting analysis, Batch Normalization, optimization algorithms, CNN hyperparameters, transfer learning, fine-tuning, and cross-validation.

A pretrained MobileNetV2 architecture was used with the base initially frozen and a new classifier head trained on the target dataset. Different weight initialization schemes such as Zero, Random, Xavier and He were compared, along with regularization techniques including L2 regularization, Dropout and Batch Normalization. Optimizers such as SGD, Momentum, RMSProp and Adam were evaluated, followed by hyperparameter analysis of learning rate, batch size and dropout rate. Transfer learning using feature extraction was compared with fine-tuning of the last layers of MobileNetV2. Finally, multiple configurations were evaluated using 5-fold cross-validation, and the best configuration was selected based on accuracy and consistency before final evaluation on the test set.  

## Dataset

**Oxford-IIIT Pet** dataset contains images of cats and dogs belonging to 37 breeds. The images are RGB and
have different spatial dimensions.  

Dataset source: [https://www.kaggle.com/datasets/tanlikesmath/the-oxfordiiit-pet-dataset](https://www.kaggle.com/datasets/tanlikesmath/the-oxfordiiit-pet-dataset)

## Repository Contents

- `Source Code.ipynb` — Colab notebook with all tasks - dataset exploration, convolution and pooling experiments, feature map visualization, model building, training, evaluation, and additional exercises.
- `Lab 5 - Comprehensive Study of CNN.pdf` — Full lab report in PDF (theory, procedure, results, plots with inferences, discussion, conclusion).
- `outputs/` — Generated plots (sample images, class distribution, kernel/stride/padding comparisons, feature maps, accuracy/loss curves, confusion matrix) as PNGs, and result table CSVs.

## How to Run

The experiments are designed to run directly in **Google Colab**.

1. Open / upload the `Source Code.ipynb` notebook in [Kaggle](https://www.kaggle.com/).
2. For better performance, go to **Settings → Accelerator** and select **GPU T4 x2** as the hardware accelerator.
3. Add the dataset mentioned above into input.
4. Run all cells using **Runtime → Run all**.
5. The notebook will automatically perform all mentioned tasks and generate the required plots and results.

No local Python environment or additional setup is required.
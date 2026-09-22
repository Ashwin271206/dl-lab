# CS3807 — Deep Learning Laboratory
## Lab 6 : End-to-End Study of RNN, LSTM and GRU for Sequence Learning and Video Understanding  

This experiment studies the complete deep learning workflow for sequence learning and video understanding using Vanilla RNN, LSTM and GRU architectures. It covers temporal data representation, sequence preprocessing, Backpropagation Through Time (BPTT), vanishing and exploding gradients, recurrent model training, performance evaluation, and comparison of RNN, LSTM and GRU models.

The primary sequence-learning task uses the UCI Human Activity Recognition Using Smartphones (HAR) dataset. Raw inertial sensor signals are arranged into temporal sequences of 128 time steps and 9 sensor channels. The experiment trains and compares SimpleRNN, LSTM and GRU models using the same experimental conditions and evaluates them using accuracy, precision, recall, F1-score, confusion matrices, parameter count and training time.

The experiment also studies the effect of sequence length using 32, 64 and 128 time steps. For video understanding, a pretrained MobileNetV2 CNN is used as a feature extractor for frames from the UCF101 action-recognition dataset, followed by an LSTM or GRU for temporal modeling. Finally, a small synthetic sequence-to-sequence reversal task is implemented using an encoder-decoder architecture.

## Dataset

- **UCI HAR** dataset contains smartphone inertial sensor measurements collected while subjects performed six activities, containing 128 temporal measurements and 9 sesnor channels from raw inertial file signals.
Dataset Source: [https://archive.ics.uci.edu/dataset/240/human+activity+recognition+using+smartphones](https://archive.ics.uci.edu/dataset/240/human+activity+recognition+using+smartphones)  

- **UCF101 Action Recognition** is used for the video-understanding portion of the experiment. It contains 101 classes and 100+ videos each.
Dataset Source : [https://www.kaggle.com/datasets/pevogam/ucf101](https://www.kaggle.com/datasets/pevogam/ucf101)

## Repository Contents

- `Source Code.ipynb` — Colab notebook with all tasks - dataset exploration, convolution and pooling experiments, feature map visualization, model building, training, evaluation, and additional exercises.
- `Lab 6 - RNN & LSTM & GRU.pdf` — Full lab report in PDF (theory, procedure, results, plots with inferences, discussion, conclusion).
- `outputs/` — Generated plots (sample images, class distribution, kernel/stride/padding comparisons, feature maps, accuracy/loss curves, confusion matrix) as PNGs, and result table CSVs.

## How to Run

The experiments are designed to run directly in **Google Colab**.

1. Open / upload the `Source Code.ipynb` notebook in [Kaggle](https://www.kaggle.com/).
2. For better performance, go to **Settings → Accelerator** and select **GPU T4 x2** as the hardware accelerator.
3. Add the UCF101 dataset from Kaggle into the input.
4. Download the UCF HAR dataset from the link, and upload the folder in Kaggle input.
5. Run all cells using **Runtime → Run all**.
6. The notebook will automatically perform all mentioned tasks and generate the required plots and results.

No local Python environment or additional setup is required.
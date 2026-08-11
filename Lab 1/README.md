# CS3807 Deep Learning Laboratory 
# Experiment 1 - Single-Layer Perceptron 

This repository contains a manual implementation of the perceptron learning algorithm, applied to two tasks:

A single-layer perceptron built using NumPy, trained to classify banknotes as authentic or forged based on four statistical features extracted from banknote images. The pipeline covers dataset exploration, preprocessing, training with the perceptron learning rule, evaluation using standard classification metrics, a learning-rate comparison, and a comparison against Scikit-learn's Perceptron implementation.

The same perceptron learning algorithm implemented independently for the AND, OR, and NOT gates, with weights displayed after every update and the decision boundary plotted at each step to visualize how the perceptron converges for each gate.

## Repository Contents

- **Code:** Google Colab notebooks containing the complete implementation for both the banknote classification task and the logic gate experiments, along with outputs.
- **Dataset:** Bank note authentication dataset in .txt format.
- **Report:** A complete PDF file documenting the objective, theory, methodology, results, and analysis for both experiments.
- **Images:** All generated plots saved in vector format.
- **Results:** Performance metrics, epoch-wise training logs, and comparison tables produced during model training and evaluation.

## How to Run

The experiments are designed to run directly in **Google Colab**.

1. Open / upload the `Source Code.ipynb` notebook in [Google Colab](https://colab.research.google.com/).
2. Upload the **Bank Note Authentication dataset** (`.txt` file) to the Colab environment.
3. For better performance, go to **Runtime → Change runtime type** and select **GPU** as the hardware accelerator.
4. Run all cells using **Runtime → Run all**.
5. The notebook will automatically perform dataset exploration, preprocessing, model training, evaluation, and generate the required plots and results.

No local Python environment or additional setup is required.
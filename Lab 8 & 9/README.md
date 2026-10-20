# CS3807 — Deep Learning Laboratory
## Experiments 8 & 9 : Effect of Attention Type and Attention Position in a Pretrained ResNet50

This experiment studies how different attention mechanisms modify an ImageNet-pretrained ResNet50 and how the position at which attention is inserted influences image-classification performance. The TensorFlow Flowers (`tf_flowers`) dataset is used to compare channel attention, spatial attention, sequential channel–spatial attention, lightweight self-attention, and combined attention.

The experiment evaluates attention type, insertion position, multiple attention positions, attention ordering, and spatial-attention kernel size. It also compares established mechanisms including Squeeze-and-Excitation (SE), Efficient Channel Attention (ECA), Convolutional Block Attention Module (CBAM), and Coordinate Attention. Models are evaluated using accuracy, precision, recall, macro F1-score, parameter count, inference time, and qualitative visualizations such as attention maps and Grad-CAM.

## Dataset

- **TensorFlow Flowers (`tf_flowers`)** contains 3,670 natural RGB flower images belonging to five classes: daisy, dandelion, roses, sunflowers, and tulips.

  Dataset Source: [TensorFlow Flowers](https://www.tensorflow.org/datasets/catalog/tf_flowers)

- All images are resized to `224 × 224 × 3` and preprocessed using the preprocessing expected by ImageNet-pretrained ResNet50. Training images use random horizontal flipping, rotations up to ±18°, zoom and translation up to ±10%, and contrast variation up to ±10%.

- The dataset is split into **70% training, 15% validation, and 15% testing**, using a stratified split with seed 42. The same saved split is reused for all experiments: 2,569 training images, 550 validation images, and 551 test images.

- In the reported run, a Protobuf version mismatch prevented `tensorflow_datasets` from importing in the Kaggle environment. The images were therefore read from the official `flower_photos` archive, which is the source used by TFDS for `tf_flowers`.

## Repository Contents

- `Source Code.ipynb` — Notebook containing dataset preparation, ResNet50 reconstruction, attention-module implementations, training, evaluation, and visualization for the experiments.
- `Lab 8 & 9 - Attention.pdf` — Full lab report containing the theory, experimental procedure, results, plots, discussion, and conclusion.
- `outputs/` — Generated figures used in the report, including sample images, performance comparisons, training curves, confusion matrices, attention maps, complexity comparisons, and Grad-CAM visualizations, and CSV files containing results

## How to Run

The experiments are designed to run in **Kaggle Notebooks**.

1. Upload or open `Source Code.ipynb` in [Kaggle](https://www.kaggle.com/).
2. Enable a GPU accelerator in the notebook settings for faster training.
3. Make the TensorFlow Flowers / official `flower_photos` dataset available to the notebook. If `tensorflow_datasets` fails because of an environment or Protobuf version mismatch, use the official `flower_photos` archive as in the reported run.
4. Ensure the image folders and class labels are mapped consistently to the five classes: dandelion, daisy, tulips, sunflowers, and roses.
5. Run the notebook cells in order.
6. The notebook trains and evaluates the baseline and attention-based models, then generates the plots and results used for comparison.

The experiments use an ImageNet-pretrained ResNet50 backbone and a fixed dataset split and augmentation setup across model comparisons. A GPU is recommended to reduce training time.

# Fashion-MNIST Image Classification with Deep Learning

An end-to-end deep learning project exploring image classification on the Fashion-MNIST dataset using PyTorch.

The project follows an iterative experimentation process, starting with a fully connected neural network and progressing toward a convolutional neural network with hyperparameter optimization, regularization, data augmentation, and adaptive learning-rate scheduling.

---

## Project Highlights

- Built a baseline Multi-Layer Perceptron (MLP) for image classification
- Performed hyperparameter optimization using Optuna
- Transitioned from fully connected layers to a CNN architecture
- Implemented convolutional feature extraction using PyTorch
- Used Batch Normalization and Dropout for regularization
- Diagnosed and resolved CNN tensor shape mismatches
- Implemented data augmentation using random rotations and translations
- Used `ReduceLROnPlateau` for adaptive learning-rate scheduling
- Analyzed train-test accuracy gaps to identify overfitting
- Compared model performance across multiple experiments

---

## Results

| Experiment | Approach | Best Test Accuracy |
|---|---|---:|
| Baseline | MLP | ~89.38% |
| Experiment 2 | CNN | ~92.42% |
| Final | CNN + Augmentation + LR Scheduling | **92.97%** |

### Final Training Run

| Metric | Result |
|---|---:|
| Best Test Accuracy | **92.97%** |
| Final Test Accuracy | 92.74% |
| Final Train Accuracy | 95.03% |
| Training Epochs | 100 |
| Initial Learning Rate | 0.001 |
| Final Learning Rate | 0.000001 |

The final model achieved a best test accuracy of 92.97%.

More importantly, the project demonstrated improved generalization after introducing data augmentation and learning-rate scheduling.

---

## Model Evolution

The project was developed iteratively:

```text
Baseline MLP
    │
    │ Hyperparameter Optimization
    ▼
Optimized MLP
    │
    │ CNN Architecture
    ▼
CNN
    │
    │ Overfitting Identified
    ▼
CNN + Regularization
    │
    │ Data Augmentation
    │ Learning Rate Scheduling
    ▼
Final CNN

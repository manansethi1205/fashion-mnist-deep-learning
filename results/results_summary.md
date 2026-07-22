# Results Summary

## Model Performance

| Experiment | Best Test Accuracy |
|---|---:|
| Baseline MLP | ~89.38% |
| CNN | ~92.42% |
| CNN + Data Augmentation + LR Scheduling | **92.97%** |

## Final Training Run

- Epochs: 100
- Best Test Accuracy: 92.97%
- Final Train Accuracy: 95.03%
- Final Test Accuracy: 92.74%
- Initial Learning Rate: 0.001
- Final Learning Rate: 0.000001

## Observations

The baseline MLP achieved approximately 89.38% test accuracy.

Moving to a CNN improved the model's ability to learn spatial features from the 28×28 input images and increased test accuracy to approximately 92.42%.

The initial CNN showed significant overfitting, with training accuracy approaching 99% while test accuracy remained around 92%.

To improve generalization, data augmentation and learning-rate scheduling were introduced.

The final model achieved a best test accuracy of 92.97%, while the final training run ended with 95.03% training accuracy and 92.74% test accuracy.

The reduced train-test gap indicates improved generalization compared with the earlier CNN experiment.

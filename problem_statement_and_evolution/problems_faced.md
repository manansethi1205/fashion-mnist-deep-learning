### Problem 1: BatchNorm Channel Mismatch

The initial CNN implementation produced a BatchNorm channel mismatch error.

The error indicated that the BatchNorm layer expected a different number of channels than the preceding convolutional layer produced.

I traced the tensor dimensions through the convolutional blocks and corrected the channel configuration.

---

### Problem 2: Fully Connected Layer Dimension Mismatch

After modifying the convolutional architecture, the flattened feature representation no longer matched the input size expected by the first Linear layer.

I validated the output shape of the CNN feature extractor using:

```python
feature_output = model.features(batch_features)

print(feature_output.shape)

flattened_size = feature_output.view(
    feature_output.size(0), -1
).shape[1]

print(flattened_size)

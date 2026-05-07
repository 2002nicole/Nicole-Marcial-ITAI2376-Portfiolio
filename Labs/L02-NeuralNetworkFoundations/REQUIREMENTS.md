# Requirements and Dependencies — L02 Neural Network Foundations Lab

This lab was designed to run in **Google Colab**, which already includes many common machine learning libraries. If running the notebook locally, install the packages listed below.

## Recommended Environment

```text
Python 3.10 or later
Google Colab recommended
GPU optional but helpful
```

## Main Dependencies

```text
numpy
matplotlib
seaborn
scikit-learn
torch
torchvision
tensorflow
keras
```

## Installation Command

If running locally, install the required libraries with:

```bash
pip install numpy matplotlib seaborn scikit-learn torch torchvision tensorflow
```

## Frameworks Used

### PyTorch

PyTorch was used to build and train a neural network with a manual training loop. This helped show each part of the training process more clearly, including:

- Forward pass
- Loss calculation
- Backpropagation
- Optimizer step
- Validation loop

### TensorFlow/Keras

TensorFlow/Keras was used to recreate a similar neural network using a higher-level API. Keras simplified the workflow through:

- `model.compile()`
- `model.fit()`
- Built-in training history
- Built-in validation tracking

## Hardware Notes

The lab can run on CPU, but using a GPU in Google Colab can make training faster.

To enable GPU in Google Colab:

1. Go to **Runtime**
2. Select **Change runtime type**
3. Choose **GPU** as the hardware accelerator
4. Save and restart the runtime

You can verify GPU availability with:

```python
import tensorflow as tf
print("GPU Available:", tf.config.list_physical_devices("GPU"))
```

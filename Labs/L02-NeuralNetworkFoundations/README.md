# L02 — Neural Network Foundations Lab

## Lab Overview

This folder contains my completed Module 02 lab for **ITAI 2376: Deep Learning**. This was a course lab, not a fully independent project. The notebook included starter code and guided sections provided by the course. My work included running the full notebook, completing the student coding sections, training models, experimenting with hyperparameters, adding dropout, completing the required student challenge, and writing reflection/analysis responses.

The purpose of this lab was to practice the foundations of neural networks by building, training, and evaluating image classification models using both **PyTorch** and **TensorFlow/Keras**.

## Problem Statement

The task was to classify images from the **Fashion-MNIST** dataset into 10 clothing categories, such as shirts, shoes, bags, and coats. The goal was not only to get good accuracy, but also to understand how neural networks learn through layers, activation functions, loss, optimization, backpropagation, and validation testing.

This lab helped connect the theory from Module 02 to practical model training.

## Source Code

The main source file for this lab is:

```text
L02_Nicole_Marcial_ITAI2376.ipynb
```

The notebook includes:

- Environment setup
- Fashion-MNIST data loading
- Data visualization
- Train/validation/test split
- PyTorch model training
- TensorFlow/Keras model training
- Hyperparameter experiments
- Dropout regularization
- Required student challenge
- Reflection and analysis responses

## Approach and Methodology

### 1. Data Preparation

The notebook loaded Fashion-MNIST, normalized the image data, and created training, validation, and test splits. The validation set was used to check model performance during training without touching the final test set.

### 2. PyTorch Model

The PyTorch model was a basic Multi-Layer Perceptron, or MLP. It flattened each 28 × 28 image into a vector and passed it through fully connected layers.

The baseline PyTorch architecture was:

```text
Flatten
Linear(784 → 512)
ReLU
Linear(512 → 512)
ReLU
Linear(512 → 10)
```

The model used:

- `CrossEntropyLoss`
- Adam optimizer
- Batch size of 64
- 10 training epochs
- Learning rate of 0.001

### 3. TensorFlow/Keras Model

The same general model structure was recreated using TensorFlow/Keras. Keras made the training workflow more concise by using `compile()` and `fit()` instead of writing a full manual training loop.

The Keras model used:

- Flatten layer
- Two dense hidden layers with ReLU activation
- Dense output layer with 10 outputs
- Adam optimizer
- Sparse categorical crossentropy loss
- Accuracy as the evaluation metric

### 4. Hyperparameter Tuning

I experimented with different learning rates, batch sizes, and epoch counts to see how the model performance changed.

The tested configurations included:

```text
Learning rate 0.01, epochs 5
Learning rate 0.0001, epochs 15
Batch size 64, learning rate 0.001, epochs 10
Batch size 128, learning rate 0.001, epochs 10
Batch size 64, learning rate 0.0005, epochs 15
```

### 5. Dropout Regularization

I added dropout layers to reduce overfitting. The dropout model used dropout after the ReLU activation layers:

```text
Linear(784 → 512)
ReLU
Dropout(0.5)
Linear(512 → 512)
ReLU
Dropout(0.5)
Linear(512 → 10)
```

### 6. Student Challenge

For the required student challenge, I implemented two main improvements:

1. Hyperparameter tuning
2. Architecture modification

For the architecture change, I reduced the model size from the original 512 → 512 hidden layer structure to a smaller 256 → 128 structure:

```text
Flatten
Linear(784 → 256)
ReLU
Linear(256 → 128)
ReLU
Linear(128 → 10)
```

I tested whether a smaller model could still perform well while potentially reducing overfitting.

## Results and Evaluation

### Baseline PyTorch Model

The baseline PyTorch model trained successfully for 10 epochs. The best validation accuracy reached approximately:

```text
Best validation accuracy: 89.08%
```

The final epoch validation accuracy was:

```text
Final validation accuracy: 88.18%
```

### TensorFlow/Keras Model

The TensorFlow/Keras model also trained successfully. It reached a final training accuracy of about 91.86%, with validation accuracy around the high 88% range.

```text
Best validation accuracy: 88.85%
Final validation accuracy: 88.49%
```

### Hyperparameter Tuning Results

The best challenge configuration was:

```text
Batch size: 64
Learning rate: 0.0005
Epochs: 15
Peak validation accuracy: 89.54%
```

This was the best result in the notebook.

### Smaller Architecture Results

The smaller MLP architecture also performed well:

```text
Architecture: 256 → 128 hidden units
Peak validation accuracy: 89.11%
```

Although it did not beat the best hyperparameter-tuned model, it showed that a smaller network could still generalize well.

### Dropout Results

The dropout model reached:

```text
Final validation accuracy: 87.90%
```

Dropout trained more slowly and produced a slightly lower validation accuracy in this lab, but the validation loss decreased more steadily. This showed how dropout can help stabilize training and reduce overfitting, even if it does not always produce the highest accuracy in a short training run.

## Learning Outcomes

From this lab, I learned how the main parts of a neural network work together during training. I practiced using both PyTorch and TensorFlow/Keras, which helped me compare a manual training loop with a higher-level framework workflow.

Key takeaways:

- PyTorch gives more control because the training loop is written step by step.
- Keras is easier to read at first because `compile()` and `fit()` handle much of the training process.
- Learning rate, batch size, and number of epochs can strongly affect validation accuracy.
- A bigger model is not always automatically better.
- Dropout can reduce overfitting by preventing the model from relying too heavily on the same neurons.
- Validation accuracy is important because it shows how well the model performs on data it did not directly train on.

## Notes About Authorship

This was a guided course lab with starter code provided as part of ITAI 2376. My contributions included completing the required coding sections, running the models, tuning hyperparameters, adding dropout, completing the student challenge experiments, and writing the reflection and analysis responses.

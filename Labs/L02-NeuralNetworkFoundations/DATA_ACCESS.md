# Sample Data and Data Access — L02 Neural Network Foundations Lab

## Dataset Used

This lab uses the **Fashion-MNIST** dataset.

Fashion-MNIST is a beginner-friendly image classification dataset containing grayscale images of clothing items. It is commonly used as an alternative to the original MNIST digit dataset because it is still simple, but slightly more realistic and challenging.

## Dataset Details

```text
Dataset: Fashion-MNIST
Image type: Grayscale clothing images
Image size: 28 × 28 pixels
Number of classes: 10
Training images: 60,000
Test images: 10,000
Total images: 70,000
```

## Classes

The dataset contains 10 clothing categories:

```text
0 - T-shirt/top
1 - Trouser
2 - Pullover
3 - Dress
4 - Coat
5 - Sandal
6 - Shirt
7 - Sneaker
8 - Bag
9 - Ankle boot
```

## Data Split Used in the Notebook

The original training data was split into a training set and validation set:

```text
Training set:   48,000 images
Validation set: 12,000 images
Test set:       10,000 images
```

## How the Data Is Accessed

No manual dataset download is required.

The notebook downloads Fashion-MNIST automatically using `torchvision.datasets.FashionMNIST`.

Example:

```python
from torchvision import datasets, transforms

train_dataset = datasets.FashionMNIST(
    root="./data",
    train=True,
    download=True,
    transform=transforms.ToTensor()
)

test_dataset = datasets.FashionMNIST(
    root="./data",
    train=False,
    download=True,
    transform=transforms.ToTensor()
)
```

When the notebook is run for the first time, the dataset is downloaded into a local `data/` folder.

## Should the Dataset Be Uploaded to GitHub?

No. The full dataset does not need to be uploaded to GitHub because it can be downloaded automatically when the notebook runs.

For this lab folder, it is enough to include:

```text
L02_Nicole_Marcial_ITAI2376.ipynb
README.md
REQUIREMENTS.md
DATA_ACCESS.md
```

## Reproducibility Notes

To reproduce the lab:

1. Open the notebook in Google Colab or Jupyter Notebook.
2. Run all cells from top to bottom.
3. Allow the notebook to download Fashion-MNIST automatically.
4. Review the training, validation, and test results shown in the notebook outputs.

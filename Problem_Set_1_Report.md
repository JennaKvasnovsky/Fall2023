# Assignment Report: MNIST Random Walk Classifier

## Introduction

This report documents the steps taken to complete the assignment, which involves the following tasks:

1. Load the MNIST dataset and visualize a montage of the images.
2. Implement a random model `y = Mx` and test it on the MNIST data.
3. Train a random walk model to achieve at least 75% accuracy on the training data.

## Step 1: MNIST Loading and Visualization

### MNIST Dataset

The MNIST dataset is a collection of 28x28 pixel grayscale images of handwritten digits (0-9). We load the dataset using the torchvision library and preprocess it for further use.

```python
train_set = datasets.MNIST('./data', train=True, download=True)
test_set = datasets.MNIST('./data', train=False, download=True)

X = train_set.data.numpy()
X_test = test_set.data.numpy()
Y = train_set.targets.numpy()
Y_test = test_set.targets.numpy()
```

### Visualization

We visualize a montage of 25 randomly selected images from the MNIST dataset using the `montage_plot` function. The montage provides a quick overview of the dataset, which is important for understanding the data we are working with.

![MNIST Montage](https://github.com/JennaKvasnovsky/Fall2023/assets/143115856/b0176120-fb26-4d80-babe-f19bac1ab625)


## Step 2: Random Model Implementation

### Random Model: `y = Mx`

For the initial exploration, we implement a simple random model `y = Mx`, where `M` is a random weight matrix of shape (10, 784), and `x` is a batch of input images. The accuracy of this random model on the MNIST data is calculated and displayed.

```python
M = np.random.rand(10, 784)
x = X[:, 0:64]  # Taking a batch of 64 images

# Calculate predictions
y = M @ x

# Find the predicted classes
y = np.argmax(y, axis=0)

# Calculate accuracy
accuracy = ((y == Y[0:64])).sum() / 64
print("Accuracy of the random model:", accuracy)
```

### Rationale for Random Model

The random model serves as a baseline to understand the expected performance of a purely random classifier. It helps us appreciate the improvement achieved through training and model refinement. The random initialization of `M` ensures that we start with a model that has no prior knowledge about the data.

## Step 3: Model Training

### Random Walk Model

To train a random walk model, we iteratively update a random weight matrix `M` using a random step and evaluate its accuracy on a batch of training data. We continue this process until the accuracy exceeds 75%.

```python
m_best = 0
acc_best = 0

for i in trange(100000):
    step = 0.000000001  # Step size
    m_random = np.random.randn(10, 784)  # Random matrix

    m = m_best + step * m_random  # Update the model with a step

    batch_index = np.random.randint(0, X.shape[1] - 1000)  # Random batch index
    y_ans = Y[batch_index:batch_index + 1000]  # True labels
    x = X[:, batch_index:batch_index + 1000]  # Input batch

    y = m @ x  # Calculate predictions
    y = np.argmax(y, axis=0)  # Predicted classes

    acc = ((y == y_ans)).sum() / 1000  # Calculate accuracy

    if acc > acc_best:
        m_best = m
        acc_best = acc

    if acc_best >= 0.75:
        break

print("Accuracy of the trained model:", acc_best)
```

### Rationale for Random Walk Model

The random walk model is an exploratory approach to finding a weight matrix `M` that performs better than the random model. Here are the key reasons behind the choices made:

- **Step Size (`step`)**: We chose a small step size to control the rate of exploration. Smaller steps result in slower exploration but reduce the risk of overshooting a good solution.

- **Random Initialization of `M`**: Similar to the random model, the random initialization of `M` ensures that we start with a model that has no prior bias.

- **Batch Selection**: We randomly select batches of training data to introduce variability in the training process and avoid getting stuck in local minima.

- **Accuracy Threshold**: We aim to achieve an accuracy of at least 75% to demonstrate that the random walk model can learn meaningful patterns from the data.


## Code for assignment
[View on Colab
](https://colab.research.google.com/drive/1q2yzCIkg_lRinrr7AuP6nTPbxx9K76gd?usp=sharing)

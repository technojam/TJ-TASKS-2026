# Level 3 Task: Building Your First Convolutional Neural Network (CNN) 🖼️⚡

Welcome! Now that you understand basic neural nodes and text routing, it is time to enter the world of **Computer Vision**. 

Images are just 2D grids of numbers (pixels). To let computers understand what is inside an image, we use Convolutional Neural Networks (CNNs). In this task, you will build and train a basic CNN from scratch using PyTorch or TensorFlow to classify simple images (like handwritten digits or clothing items).

---

## 🧠 Understanding the Concept

A CNN mimics the human visual cortex using three core layers:
1. **Convolutional Layers:** Slide small filters (kernels) across the image to automatically detect edges, shapes, and patterns.
2. **Pooling Layers:** Shrink the image size (downsampling) to reduce computation and keep only the most important features.
3. **Fully Connected (Dense) Layers:** Take the extracted features and make the final classification choice.

---

## 📝 The Official Task

### Objective
Write a Python script using **PyTorch** (or TensorFlow/Keras) to build a small CNN that classifies images from the built-in `MNIST` (handwritten digits).
### Requirements
1. **Load and Normalize Data:** Load the dataset and normalize pixel values from ranges `[0, 255]` down to `[0, 1]`.
2. **Define the CNN Architecture:** 
   * Conv2D layer (e.g., 32 filters, 3x3 kernel) + ReLU activation + MaxPool2D layer.
   * Flatten layer to convert 2D maps into a 1D vector.
   * Dense output layer with 10 units (for classes 0-9).
3. **Train the Model:** Set up a simple training loop using Cross-Entropy Loss and an optimizer (like Adam) for at least **1 to 3 epochs**.
4. **Evaluate:** Print the final test accuracy.

### Starter Template (PyTorch)
```python
import torch
import torch.nn as nn
import torch.optim as optim
from torchvision import datasets, transforms
from torch.utils.data import DataLoader

# 1. Load dataset & apply normalization
transform = transforms.Compose([transforms.ToTensor(), transforms.Normalize((0.5,), (0.5,))])
trainset = datasets.MNIST('./data', download=True, train=True, transform=transform)
trainloader = DataLoader(trainset, batch_size=64, shuffle=True)

# 2. Define the CNN Model
class SimpleCNN(nn.Module):
    def __init__(self):
        super(SimpleCNN, self).__init__()
        self.conv1 = nn.Conv2d(1, 16, kernel_size=3, stride=1, padding=1)
        self.pool = nn.MaxPool2d(kernel_size=2, stride=2)
        self.fc1 = nn.Linear(16 * 14 * 14, 10) # MNIST images are 28x28, halved by pooling to 14x14

    def forward(self, x):
        x = self.pool(torch.relu(self.conv1(x)))
        x = x.view(-1, 16 * 14 * 14) # Flatten
        x = self.fc1(x)
        return x

model = SimpleCNN()
print(model)
```
# Resources
You can use google colab and kaggle to train and for datasets
``` 
Dataset : https://www.kaggle.com/datasets/hojjatk/mnist-dataset
Colab : https://colab.research.google.com
```
Youtube video link : https://www.youtube.com/watch?v=dsDPre8EVgM

Documentation link : https://www.kaggle.com/code/itsmohammadshahid/7-cnn-handwritten-digit-recognition
# Project Proposal Overview 

## Libraries and MNIST dataset

### 1. Check the device and import modules 

```python
import torch

# Import the torch library, which is a popular deep learning framework

# Device configuration
device = torch.device('cuda' if torch.cuda.is_available() else 'cpu')
# Check if a CUDA-enabled GPU is available using torch.cuda.is_available()
# If GPU is available, set device to 'cuda' to run code on GPU
# If GPU is not available, set device to 'cpu' to run code on CPU

# Print the selected device ('cuda' or 'cpu')
print(device)

# Import the necessary modules
# Import the datasets module from torchvision library
# The torchvision library provides popular datasets like MNIST, CIFAR10, etc.
# These datasets can be used for computer vision tasks
from torchvision import datasets

# Import the ToTensor class from the transforms module in torchvision
# The ToTensor transform is used to convert input data, such as images, into PyTorch tensors
# It ensures that the data is in the appropriate format for deep learning tasks
from torchvision.transforms import ToTensor
```

By importing these modules and using the provided functionalities:

The datasets module allows you to work with pre-built datasets like MNIST, CIFAR10, etc., which are commonly used in computer vision tasks.
The ToTensor class from the transforms module allows you to convert data, such as images, into PyTorch tensors, which is the appropriate format for deep learning models.
These imports enable you to load and process datasets, as well as convert the data into a suitable format for training and inference with deep learning models.

### 2. Get the dataset  
```python
# Import the necessary modules
from torchvision import datasets
from torchvision.transforms import ToTensor

# Download the MNIST training dataset
train_data = datasets.MNIST(
    root='data',              # Root directory where the dataset will be stored
    train=True,               # Download the training split of the dataset
    transform=ToTensor(),     # Convert the image to a PyTorch tensor
    download=True,            # Download the dataset if it doesn't exist
)

# Download the MNIST test dataset
test_data = datasets.MNIST(
    root='data',              # Root directory where the dataset will be stored
    train=False,              # Download the test split of the dataset
    transform=ToTensor(),     # Convert the image to a PyTorch tensor
)

# Print information about the training dataset
print(train_data)
print(train_data.data.size())       # Size/shape of the input images
print(train_data.targets.size())    # Number of labels in the training dataset
```


```python
# Import the necessary modules
from torchvision import datasets
from torchvision.transforms import ToTensor

# Download the MNIST training dataset
train_data = datasets.MNIST(
    root='data',              # Root directory where the dataset will be stored
    train=True,               # Download the training split of the dataset
    transform=ToTensor(),     # Convert the image to a PyTorch tensor
    download=True,            # Download the dataset if it doesn't exist
)

# Download the MNIST test dataset
test_data = datasets.MNIST(
    root='data',              # Root directory where the dataset will be stored
    train=False,              # Download the test split of the dataset
    transform=ToTensor(),     # Convert the image to a PyTorch tensor
)

# Print information about the training dataset
print(train_data)
print(train_data.data.size())       # Size/shape of the input images
print(train_data.targets.size())    # Number of labels in the training dataset
```

1. `datasets.MNIST`: This is a class provided by the torchvision library that represents the MNIST dataset. It allows you to download and work with the MNIST dataset conveniently. When creating an instance of this class, you can pass various parameters to customize its behavior. In the code, `datasets.MNIST()` is used to create instances for both the training and test datasets.

2. `root`: This parameter specifies the root directory where the downloaded dataset will be stored. In the code, `'data'` is used as the root directory. If the directory doesn't exist, it will be created.

3. `train`: This parameter determines whether to download the training split of the dataset. By setting it to `True`, the code downloads the training data. When set to `False`, it downloads the test data.

4. `transform`: This parameter allows you to specify any transformations that should be applied to the dataset. In the code, `ToTensor()` is used, which converts the input images from the dataset into PyTorch tensors. This transformation is necessary because most deep learning frameworks, including PyTorch, work with tensors as the input data format.

5. `download`: This parameter specifies whether to download the dataset if it doesn't already exist. By setting it to `True`, the code will download the dataset. If the dataset is already present in the specified `root` directory, it will not be re-downloaded.

6. `train_data.data`: This attribute of the `MNIST` dataset object represents the input images in the training dataset. It contains the pixel values of the images.

7. `train_data.targets`: This attribute represents the labels corresponding to the input images in the training dataset. It contains the ground-truth values for each image.

8. `size()`: This is a method available for PyTorch tensors. It returns the size or shape of a tensor. In the code, `train_data.data.size()` is used to get the size of the input images tensor, and `train_data.targets.size()` is used to get the size of the labels tensor.

By using the `datasets.MNIST` class and these functions, you can conveniently download the MNIST dataset and access its images and labels for further processing or training machine learning models.

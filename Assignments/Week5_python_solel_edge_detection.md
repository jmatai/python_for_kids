## Assignment 5: Sobel edge detection
1) Read this document and understand the sobel edge detection
2) Complete the python code for solel edge detection 
   - Create a sobel_edge_detection.py file
   - Push your code to https://github.com/Damouiii/MyPythonProject 
   
## Sobel Edge Detection

Sobel edge detection is a popular method for detecting edges in an image. It works by convolving the image with a small kernel, usually a 3x3 or 5x5 matrix, and calculating the gradient magnitude at each pixel. The gradient magnitude is a measure of the rate of change of the image intensity, and it is higher at pixels where there is a sudden change in intensity, such as at an edge.

The Sobel operator consists of two separate kernels: one for detecting edges in the x direction and one for detecting edges in the y direction. The x-direction kernel emphasizes vertical edges and the y-direction kernel emphasizes horizontal edges. These two kernels are then applied separately to the image, and the results are combined to produce the final edge detection output.

### Mathematically Applying the Filters

The Sobel operator is a discrete differentiator, meaning that it approximates the gradient of the image intensity function at each pixel. The x and y direction kernels are defined as:

```python
          _               _                   _                _
         |                 |                 |                  |
         | 1.0   0.0  -1.0 |                 |  1.0   2.0   1.0 |
    Gx = | 2.0   0.0  -2.0 |    and     Gy = |  0.0   0.0   0.0 |
         | 1.0   0.0  -1.0 |                 | -1.0  -2.0  -1.0 |
         |_               _|                 |_                _|
```

To apply these kernels to an image, we convolve the kernel with the image at each pixel. The convolution operation involves sliding the kernel over the image and computing the dot product of the kernel with the image values at each position. The result of this operation at each pixel is a single scalar value representing the intensity gradient in the x or y direction.

### Python Code for Sobel Edge Detection

Here is a template code for python sobel edge detection 


```python
# import necessary libraries
from PIL import Image
import numpy as np

def convolve(image, filter):
    """
    :param image: An input image
    :param filter: A filter
    :return: Convolved image
    """

def sobel_edge_detection(image):
    """
    :param image: An numpy array of that should be processed with sobel filter

    The kernels Gx and Gy can be thought of as a differential operation in the "input_image" array in the directions x and y
    respectively. These kernels are represented by the following matrices:
          _               _                   _                _
         |                 |                 |                  |
         | 1.0   0.0  -1.0 |                 |  1.0   2.0   1.0 |
    Gx = | 2.0   0.0  -2.0 |    and     Gy = |  0.0   0.0   0.0 |
         | 1.0   0.0  -1.0 |                 | -1.0  -2.0  -1.0 |
         |_               _|                 |_                _|

    The sobel edge detection works by convolving the input image with Gx, then Gy, and storing the sqrt of (GxGx + Gy*Gy) into the output image.

    Following is a codoe that explains the sobel edge detection:

    Gx_image = convolve(image, Gx)
    Gy_image = convolve(image, Gy)
    output_image = np.sqrt(np.square(Gx_image) + np.square(Gy_image))

    :return: Returns an numpy which is output_image. THe output_image is an array that is the result of applying Gx and Gy as shown above. 
    """

    # Define the matrices associated with the Sobel filter
    Gx = np.array([[1.0, 0.0, -1.0], [2.0, 0.0, -2.0], [1.0, 0.0, -1.0]])
    Gy = np.array([[1.0, 2.0, 1.0], [0.0, 0.0, 0.0], [-1.0, -2.0, -1.0]])

    # Get the shape of the input grayscale image
    [rows, columns] = image.shape

    # Write your code here.
    # Here, the Sobel filter is applied to the input image using the Gx and Gy kernels
    # and the resulting image is returned
    Gx_image = convolve(image, Gx)
    Gy_image = convolve(image, Gy)
    output_image = np.sqrt(np.square(Gx_image) + np.square(Gy_image))

    return output_image


if __name__ == "__main__":
    # Load and convert the input image to grayscale
    img = Image.open('Valve_original.png').convert('L')
    img.save('greyscale.png')

    # Convert the image to a numpy array
    image = np.array(img)

    # Apply the Sobel filter to the input image
    sobel_result = sobel_edge_detection(image)

    # Create a PIL image from the numpy array and display it
    img = Image.fromarray(np.uint8(sobel_result * 255), 'L')
    img.show()

    # Save the result to a file
    img.save('sobel_result.png')

```


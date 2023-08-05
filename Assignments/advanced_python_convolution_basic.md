# Convolution 

## Convolution code 

Below, we provide a convolution which is the main block of convolutional neural networks.   

1) The followng code works for 3x3 filter(F) size and 4x4 image (I). Please make sure you can run this code.
2) Please chaning the dimension of input image (I), and observe how this impacts the output?  Change the dimension of I from 4x4 to several different dimensions such as 5x5, 6x6, 8x8, 10x10, 15x15 and 100x100. 
3) For all the above shapes, please print the output dimension.     
Optional: 4) Suppose you have an input image I of shape (6, 6) and a filter F of shape (3, 3). According to the provided code, the convolution operation will be applied to the input image using the given filter. What will be the shape of the resulting output image I_out after applying the convolution? Explain how the change in the input image shape affects the output shape in this scenario.


```python
import numpy as np

def convolve(image, filter):
    """
    :param image: An input image I
    :param filter: A filter F
    :return: Convolved image O
    """
    out_dim1 = len(image) - 2
    out_dim2 = len(image[0]) - 2

    # Initialize the output image with zeros
    img_out = np.zeros([out_dim1, out_dim2])

    # Iterate over each pixel in the output image
    for i in range(out_dim1):  # going over the number of rows
        for j in range(out_dim2):  # going over the number of columns
            res = 0

            # Apply the convolution operation by iterating over the filter
            for m in range(-1, 2):  # it iterates 3 times => RUNS for 3 times
                for n in range(-1, 2):  # it iterates 3 times => RUNS for 3 times
                    # Perform the convolution by multiplying the filter with the corresponding image pixel
                    res += filter[m + 1][n + 1] * image[i + m + 1][j + n + 1]

            # Save the result of the convolution at the current position in the output image
            img_out[i][j] = res

    return img_out


if __name__ == "__main__":
    # Input image, a 4x4 matrix with random integer values from 0 to 9
    I = np.random.randint(10, size=(4, 4))

    # Filter for convolution, Gx is the Sobel operator for edge detection in the x-direction
    F = np.array([[-1.0, 0.0, 1.0], [-2.0, 0.0, 2.0], [-1.0, 0.0, 1.0]])

    # Perform the convolution of the input image with the filter
    I_out = convolve(I, F)

    # Print the resulting convolved image
    print("Output is \n {}".format(I_out))
	
	# Print the resulting convolved image
    print("Output shape is \n {}".format(I_out.shape))







```
# Assignment 3


## Part 1

[Review the classes from this link. ](https://github.com/jmatai/python_for_kids/blob/main/Week5_python_classes.md)


## Part 2

Design a Vector (let us name it SuperVector class) class in python that can add, subtract and multiply vectors of any size. For example, the Vector class from Part 1 only works for vector sizes of 3. Use the Vector class from Part 1 if necessary.   

Here is the Vector class from Part 1.  
```python
class Vector:
    def __init__(self, x, y, z):
        self.x = x
        self.y = y
        self.z = z
    
    def add(self, other):
        return Vector(self.x + other.x, self.y + other.y, self.z + other.z)
    
    def subtract(self, other):
        return Vector(self.x - other.x, self.y - other.y, self.z - other.z)
    
    def multiply(self, scalar):
        return Vector(self.x * scalar, self.y * scalar, self.z * scalar)
    
    def __str__(self):
        return f"({self.x}, {self.y}, {self.z})"

```

## Part 3

Write a python function that takes two matrices (A and B) as an input, and this function should output the multiplication of these two matrices as C. Below is a pseudo code is goven for you. 

```python
# Initialize two matrices A and B
# Check if A's number of columns is equal to B's number of rows
# If not, print an error message and exit

# Initialize a new matrix C with the same number of rows as A and the same number of columns as B

# Loop over the rows i of A:
#     Loop over the columns j of B:
#         Initialize a variable sum to 0
#         Loop over the elements k of row i of A and column j of B:
#             Add the product of A[i][k] and B[k][j] to sum
#         Set C[i][j] to sum

# Print matrix C


```

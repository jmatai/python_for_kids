# Python Class

Python is an object-oriented programming language, which means that it supports the creation of objects and classes. Classes are like blueprints or templates for creating objects.

A class defines a set of attributes and methods that an object of that class can have. Attributes are variables that belong to an object, while methods are functions that an object can perform.

## Introduction to Python Classes 
Here's an example of a simple Python class:

```python
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age
        
    def greet(self):
        print(f"Hello, my name is {self.name} and I am {self.age} years old.")

```


In this example, we've defined a Person class with two attributes (name and age) and one method (greet).

The __init__ method is a special method that is called when an object is created from the class. It takes in two parameters (name and age) and assigns them to the name and age attributes of the object. The self parameter refers to the object that is being created.

The greet method is a simple method that prints a greeting message to the console, using the name and age attributes of the object. The self parameter is again used to refer to the object.

Now, we can create objects (also known as instances) of the Person class:



```python
person1 = Person("Alice", 30)
person2 = Person("Bob", 25)

```
We've created two Person objects here - person1 and person2. We've passed in the name and age parameters to the Person constructor, which has created two separate objects with their own name and age attributes.

We can now call the greet method on these objects:

```python
person1.greet()  # Output: Hello, my name is Alice and I am 30 years old.
person2.greet()  # Output: Hello, my name is Bob and I am 25 years old.

```
Calling the greet method on the person1 and person2 objects will print out their respective greeting messages to the console.


## Python Vector Class
Here is an example of creating Vector class for Vector operations. 
 
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

		
This class defines a three-dimensional vector with x, y, and z components. It has methods for adding, subtracting, and multiplying vectors, as well as a __str__ method that returns a string representation of the vector.

Here's an example of how you can use this class:

```python
v1 = Vector(1, 2, 3)
v2 = Vector(4, 5, 6)

v3 = v1.add(v2)
print(v3)  # Output: (5, 7, 9)

v4 = v2.subtract(v1)
print(v4)  # Output: (3, 3, 3)

v5 = v1.multiply(2)
print(v5)  # Output: (2, 4, 6)
```

In this example, we create two vectors v1 and v2 with components (1, 2, 3) and (4, 5, 6), respectively. We then use the add, subtract, and multiply methods to perform vector operations on these vectors. Finally, we print the resulting vectors using the __str__ method.


## Python Matrix Operations

$$
\left(\begin{array}{cc} 
\color{red} a_{1,1} & 0.4472136\\
-0.4472136 & -0.8944272
\end{array}\right)
\left(\begin{array}{cc} 
10 & 0\\ 
0 & 5
\end{array}\right)
$$ 

Let A be an m x n matrix and B be an n x p matrix. Then, the product of A and B, denoted by AB, is an m x p matrix defined as follows:

- The element in row i and column j of AB is obtained by multiplying the elements in the ith row of A with the elements in the jth column of B, and summing the products. That is:

  (AB)_ij = a_i1 * b_1j + a_i2 * b_2j + ... + a_in * b_nj

  In other words, the (i,j)th entry of AB is the dot product of the ith row of A and the jth column of B.

Note that for the product AB to be defined, the number of columns in A must be equal to the number of rows in B.
# Python Class Practice  


## SuperVector Class 

The goal of this assignment is to esign a Vector (let us name it SuperVector class) class in python that can add, subtract and multiply vectors of **any size**. For example, the Vector class from Part 1 only works for vector sizes of 3. Use the Vector class from Part 1 if necessary.   


```python
v1 = SuperVector([1, 2, 3])
v2 = SuperVector([4, 5, 6])

print(v1 + v2)      # Output: Vector([5, 7, 9])
print(v1 - v2)      # Output: Vector([-3, -3, -3])
print(v1 * v2)      # Output: 32

```

Or it can also take vector of size 4, and us the same class to calculate add, subtract or multiply as follows. 

```python
v1 = SuperVector([1, 2, 3, 100])
v2 = SuperVector([4, 5, 6, 100])

print(v1 + v2)      # Output: Vector([5, 7, 9, 200])
print(v1 - v2)      # Output: Vector([-3, -3, -3, 0])
print(v1 * v2)      # Output: 10032

```

### SuperVector Class Version 1
In this section, we start designing a SuperVector class, but we do not use operator overloading (operator overloading will be explained later). Thus, in order to add two vectors, we use a method like this v1.add(v2). More specifically, we use the SuperVector as follows. 

```python
v1 = SuperVector([1, 2, 3])
v2 = SuperVector([4, 5, 6])

res = v1.add(v2)
print(res)          # Output: Vector([5, 7, 9, 200])

res = v1.sub(v2)
print(res)          # Output: Vector(-3, -3, -3) 

res = v1.mul(v2)
print(res)          # Output: 32

```

Here is an initial design of SuperVector class. 

```python
class SuperVector:
    # The constructor takes a list of components and initializes the object
    def __init__(self, components):
        self.components = components

    # The add method takes another SuperVector object and returns the sum of the two vectors
    def add(self, other):
        # Check that the vectors have the same size
        if len(self.components) != len(other.components):
            raise ValueError("Vectors must be of the same size to add.")

        # Create an empty list to hold the result
        result = []
        # Iterate over the indices of the components
        for i in range(len(self.components)):
            # Add the corresponding components and append the result to the result list
            result.append(self.components[i] + other.components[i])

        # Return a new SuperVector object with the resulting components
        return SuperVector(result)

    # The sub method takes another SuperVector object and returns the difference of the two vectors
    def sub(self, other):
        # Check that the vectors have the same size
        if len(self.components) != len(other.components):
            raise ValueError("Vectors must be of the same size to subtract.")

        # Create an empty list to hold the result
        result = []
        # Iterate over the indices of the components
        for i in range(len(self.components)):
            # Subtract the corresponding components and append the result to the result list
            result.append(self.components[i] - other.components[i])

        # Return a new SuperVector object with the resulting components
        return SuperVector(result)

    # The mul method takes another SuperVector object and returns the dot product of the two vectors
    def mul(self, other):
        # Check that the vectors have the same size
        if len(self.components) != len(other.components):
            raise ValueError("Vectors must be of the same size to multiply.")

        # Initialize the result to zero
        result = 0
        # Iterate over the indices of the components
        for i in range(len(self.components)):
            # Multiply the corresponding components and add the result to the running total
            result += (self.components[i] * other.components[i])

        # Return the final result
        return result

    # The __repr__ method returns a string representation of the object
    def __repr__(self):
        return f"Vector({self.components})"

```


The SuperVector class four four methods:

- __init__: This is the constructor method. It takes a list of components and initializes the object's components attribute.
- add: This method takes another SuperVector object and returns the sum of the two vectors. It checks that the vectors have the same size, creates a new list to hold the result, iterates over the indices of the components, adds the corresponding components, and appends the result to the result list. Finally, it returns a new SuperVector object with the resulting components.
- sub: This method is similar to add, but it subtracts the corresponding components of the two vectors instead of adding them.
- mul: This method takes another SuperVector object and returns the dot product of the two vectors. It checks that the vectors have the same size, initializes the result to zero, iterates over the indices of the components, multiplies the corresponding components, and adds the result to the running total. Finally, it returns the final result.
- __repr__: This is a special method that returns a string representation of the SuperVector object. In this case, it returns a string that includes the object's components attribute.

Question: Why we say SuperVector has four methods? 


### SuperVector Class Version 2
We modify the above code so that we can call the SuperVector as follows.  


```python
v1 = SuperVector([1, 2, 3])
v2 = SuperVector([4, 5, 6])

print(v1 + v2)      # Output: Vector([5, 7, 9])
print(v1 - v2)      # Output: Vector([-3, -3, -3])
print(v1 * v2)      # Output: 32

```

Here is the solution using **operator overloading**  

Operator overloading is a feature in Python (and many other programming languages) that allows operators such as +, -, *, / etc. to be redefined and behave differently depending on the context in which they are used.

In Python, operator overloading is achieved by defining special methods for classes that correspond to the specific operator being overloaded. These methods are known as "magic" or "dunder" methods, because they have double underscores (__) before and after their names.

For example, to overload the + operator for a custom class SuperVector, you can define a special method __add__(self, other) inside the class, where self refers to the instance of the class and other refers to the other operand being added to it. Similarly, to overload the - operator, you can define the __sub__(self, other) method, and so on for other operators.

By defining these methods, you can customize the behavior of operators for instances of your own class. This can be useful when you want to create a custom data type and define how it should behave under different arithmetic operations.

Here's an example to illustrate operator overloading using SuperVector class:


```python
class SuperVector:
    def __init__(self, components):
        self.components = components

    def __add__(self, other):
        if len(self.components) != len(other.components):
            raise ValueError("Vectors must be of the same size to add.")

        result = []
        for i in range(len(self.components)):
            result.append(self.components[i] + other.components[i])

        return SuperVector(result)

    def __sub__(self, other):
        if len(self.components) != len(other.components):
            raise ValueError("Vectors must be of the same size to subtract.")

        result = []
        for i in range(len(self.components)):
            result.append(self.components[i] - other.components[i])

        return SuperVector(result)

    def __mul__(self, other):
        if len(self.components) != len(other.components):
            raise ValueError("Vectors must be of the same size to multiply.")

        result = 0
        for i in range(len(self.components)):
            result += (self.components[i] * other.components[i])

        return result

    def __repr__(self):
        return f"Vector({self.components})"


```

- The \__add\__ method is defined to overload the + operator, so that we can add two SuperVector instances using the + operator. It takes the second vector as the other parameter and checks if the two vectors are of the same size. If they are not, it raises a ValueError exception. Otherwise, it creates a new vector whose components are the sum of the corresponding components of the two vectors, and returns it as a new SuperVector instance.

- The \__sub\__ method is defined to overload the - operator, so that we can subtract two SuperVector instances using the - operator. It takes the second vector as the other parameter and checks if the two vectors are of the same size. If they are not, it raises a ValueError exception. Otherwise, it creates a new vector whose components are the difference of the corresponding components of the two vectors, and returns it as a new SuperVector instance.

- The \__mul\__ method is defined to overload the * operator, so that we can perform dot product of two SuperVector instances using the * operator. It takes the second vector as the other parameter and checks if the two vectors are of the same size. If they are not, it raises a ValueError exception. Otherwise, it calculates the dot product of the two vectors, and returns it as a scalar value.



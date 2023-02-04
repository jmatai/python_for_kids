# Python Variables

In Python, a variable is a named location in memory that stores a value. Variables can be of different types, such as integer, float, and string.

## Integer Variables
An integer variable is a variable that stores an integer (whole number) value. The value can be positive or negative. 
For example:
```python
x = 5
y = -3 
```

## Python Float Type Variable

A float, or floating point number, is a type of number in Python that contains a decimal point. These numbers are useful for mathematical calculations that require precision.

A float variable is a variable that stores a float value. The value can be positive or negative. Here is an example of a float variable:
```python
pi = 3.14159

print(pi)
# Output: 3.14159
```


## Python String Type Variable


A string, in Python, is a sequence of characters enclosed in either single or double quotes. It can be used to represent text or a sequence of characters.

A string variable is a variable that stores a string value. Here is an example of a string variable:
```python
name = "Alice"
print(name)
# Output: Alice 

last_name = "Smith"
full_name = name + " " + last_name
print(full_name)
# Output: Alice Smith
```


### String Functions
In Python, there are many built-in functions that you can use to manipulate strings. Here are a few of the most commonly used string functions:

len(string): Returns the length of the string.

```python
string = "Hello, World!"
print(len(string)) # prints 13
```

str.upper(): Returns a copy of the string in uppercase.
```python
string = "Hello, World!"
print(string.upper()) # prints "HELLO, WORLD!"
```

str.lower(): Returns a copy of the string in lowercase.

```python
string = "Hello, World!"
print(string.lower()) # prints "hello, world!"
```
	

### Looping through a String
You can use a for loop to iterate over each character in a string. Here's an example:

```python
string = "Hello, World!"
for char in string:
    print(char)
```
This will print each character in the string on a new line.


### Indexing a String
In Python, you can access individual characters in a string using indexing. The index of the first character in the string is 0, and the index of the last character is len(string) - 1. Here's an example:

```python
string = "Hello, World!"
print(string[0]) # prints "H"
print(string[-1]) # prints "!"
```

You can also use slicing to extract a portion of the string. The syntax is string[start:end], where start is the index of the first character to include in the slice, and end is the index of the first character to exclude from the slice. If start is not specified, it defaults to 0. If end is not specified, it defaults to len(string). Here's an example:


```python
string = "Hello, World!"
print(string[7:12]) # prints "World"
```


# Python Data Structures 
In Python, a list is a collection of items that are ordered and changeable. Lists are defined by square brackets [] and items are separated by commas.

Here is an example of a list of numbers:
```python
numbers = [1, 2, 3, 4, 5]

```


You can access the items in a list by referring to the index number:

```python
print(numbers[0]) # Output: 1
print(numbers[2]) # Output: 3
```

You can change the value of a specific item by referring to the index number:

```python
numbers[2] = 6
print(numbers) # Output: [1, 2, 6, 4, 5]

```

You can loop through a list using a for loop:

```python
for number in numbers:
    print(number)
# Output:
# 1
# 2
# 6
# 4
# 5

```

You can add an item to the end of a list using the append() method:
```python
numbers.append(7)
print(numbers) # Output: [1, 2, 6, 4, 5, 7]
```

You can insert an item at a specific position using the insert() method:
```python
numbers.insert(2, 3)
print(numbers) # Output: [1, 2, 3, 6, 4, 5, 7]
```

You can remove an item using the remove() method:

```python
numbers.remove(6)
print(numbers) # Output: [1, 2, 3, 4, 5, 7]
```

Here are more examples of using list in python. 

```python
cars = ["Tesla", "Mercedes", "BMW", "Porsche", "Ferrari"]
print("My favorite car is a " + cars[3])
```

You can iterate the list with conditional to print specific car you like programmatically. 

```python
cars = ["Tesla", "Mercedes", "BMW", "Porsche", "Ferrari"]
for x in cars:
    if x=="Porsche":
        print(x)
		
# This will print Porsche
```

# If-Else Statement in Python

An if-else statement in Python is a control flow statement that allows you to execute a certain code block only if a given condition is true, and another code block if the condition is false. The basic syntax is as follows:

```python
if condition:
    # code to be executed if condition is True
else:
    # code to be executed if condition is False
```
	
For example, consider the following code:
```
x = 10
if x > 5:
    print("x is greater than 5")
else:
    print("x is not greater than 5")
```
This code will print "x is greater than 5" because the condition (x > 5) is true.

It's also possible to use multiple conditions in an if-else statement using the elif keyword:

```
x = 10
if x > 15:
    print("x is greater than 15")
elif x > 5:
    print("x is greater than 5 but not greater than 15")
else:
    print("x is not greater than 5")
```
This code will print "x is greater than 5 but not greater than 15".



# For Loops in Python

The for loop in Python is used to iterate over a sequence (such as a list, tuple, or string) and execute a block of code for each item in the sequence. The basic syntax is as follows:

```python
for item in sequence:
    # Code to be executed for each item in the sequence
```
Here's an example that uses a for loop to print each item in a list:

```python
fruits = ['apple', 'banana', 'cherry']
for fruit in fruits:
    print(fruit)
```

This code will print each fruit in the list on a new line:
```python
apple
banana
cherry
```

It's also possible to use the range function to generate a sequence of numbers, and then use a for loop to iterate over the numbers. The range function generates a sequence of numbers from start to stop-1. Here's an example:

```python
for i in range(5):
    print(i)
```
This code will print the numbers from 0 to 4:

```python
0
1
2
3
4
```
You can also specify a step value to skip numbers in the sequence. Here's an example:

```python
for i in range(0, 10, 2):
    print(i)
```
This code will print the even numbers from 0 to 8:

```python
0
2
4
6
8
```

# Python Functions 
Here is the basic syntax for defining a function in Python:

```python
def function_name(parameters):
    # code to be executed
    return [expression]
```
	
where function_name is the name of the function, parameters are the input arguments to the function and return [expression] is an optional return statement that returns a value from the function.

## Example: Adding two numbers
Here is an example of a function that takes two parameters as input and returns their sum:

```python
def add_numbers(a, b):
    return a + b

result = add_numbers(3, 4)
print(result)
```
This code will output:

```python
7
```


## Example: Multiplying two numbers

Here is an example of a function that takes two parameters as input and returns their product:

```python
def multiply_numbers(a, b):
    return a * b

result = multiply_numbers(3, 4)
print(result)
```
This code will output:

```python
12
```
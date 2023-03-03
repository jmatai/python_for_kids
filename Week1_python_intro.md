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

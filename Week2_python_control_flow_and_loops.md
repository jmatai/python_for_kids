# Python Control Flow and Loops 

In Python, a variable is a named location in memory that stores a value. Variables can be of different types, such as integer, float, and string.

	

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

```
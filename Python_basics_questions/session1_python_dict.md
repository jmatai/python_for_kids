# Assignment - Dictionary 

Please read the Part 1 and understand the basics of dictionaries, and answers the questions from Part 2. 

## Part 1: Dictionaries in Python 

In Python, a dictionary is a built-in data structure that stores key-value pairs. It is sometimes also referred to as an associative array, map, or hash table in other programming languages.

The keys in a dictionary must be unique and immutable, while the values can be of any type (including other dictionaries). Dictionaries are mutable, which means that you can add, remove, and modify key-value pairs after the dictionary has been created.

Here is an example of how to create a dictionary in Python:

```python
# Create an empty dictionary
my_dict = {}

# Create a dictionary with some key-value pairs
my_dict = {'apple': 2.99, 'banana': 0.99, 'orange': 1.50}

```

In the first example, we create an empty dictionary by assigning {} to the variable my_dict. In the second example, we create a dictionary with three key-value pairs, where the keys are strings and the values are floating-point numbers.

Here are some examples of how to perform operations on a dictionary:

```python
# Add a new key-value pair to the dictionary
my_dict['grape'] = 2.00

# Access the value associated with a particular key
price_of_apple = my_dict['apple']

# Check if a key is in the dictionary
is_banana_in_dict = 'banana' in my_dict

# Iterate over the keys and values in the dictionary
for fruit, price in my_dict.items():
    print(fruit, price)

# Remove a key-value pair from the dictionary
del my_dict['orange']

```

In the first example, we add a new key-value pair to the dictionary using square bracket notation. In the second example, we access the value associated with the key 'apple' and assign it to the variable price_of_apple. In the third example, we check if the key 'banana' is in the dictionary and assign the result to the variable is_banana_in_dict. In the fourth example, we iterate over the keys and values in the dictionary using the items() method, and print each key-value pair. In the fifth example, we remove the key-value pair associated with the key 'orange' from the dictionary using the del statement.


## Part 2: Questions  

- What is a dictionary in Python, and how is it different from a list?
- How do you create a new dictionary in Python?
- How do you add a new key-value pair to a dictionary?
- How do you access the value associated with a particular key in a dictionary?
- How do you check if a key is in a dictionary?
- How do you iterate over the keys and values in a dictionary?
- How do you remove a key-value pair from a dictionary?
- What is the difference between the get() method and the square bracket notation for accessing a value in a dictionary?
- How do you clear all the key-value pairs from a dictionary?
- How do you create a dictionary from two lists, where one list contains keys and the other list contains values?


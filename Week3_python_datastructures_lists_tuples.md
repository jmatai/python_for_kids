# Python Data Structures 

## Python Lists 
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

## Python Tuples  
In Python, a tuple is an ordered, immutable sequence of elements. This means that once a tuple is created, its contents cannot be modified. Tuples are similar to lists, but with one key difference: lists are mutable, while tuples are immutable.

Tuples are created using parentheses () and separating the elements with commas ,. For example:
```python
my_tuple = (1, 2, 3)
```

Tuples can also be created without the parentheses, but it is recommended to use them for clarity:
```python
my_tuple = 1, 2, 3
```

### Examples of using tuples in Python

Accessing elements of a tuple:
To access elements of a tuple, you can use indexing. Indexing starts at 0 for the first element, and negative indexing starts at -1 for the last element. For example:
```python
my_tuple = (1, 2, 3)

print(my_tuple[0])  # Output: 1
print(my_tuple[-1])  # Output: 3
```

Immutable nature of tuples:
Since tuples are immutable, you cannot modify their contents. Attempting to do so will result in a TypeError. For example:
```python
my_tuple = (1, 2, 3)

my_tuple[0] = 4  # Raises a TypeError: 'tuple' object does not support item assignment
```

Using tuples for multiple assignments:
Tuples can also be used for multiple assignments in a single line. This can be useful when you want to assign values to multiple variables at once. For example:
```python
my_tuple = (1, 2, 3)

a, b, c = my_tuple

print(a)  # Output: 1
print(b)  # Output: 2
print(c)  # Output: 3
```

Using tuples as function return values:
Tuples are often used to return multiple values from a function. For example:
```python
def get_name_and_age():
    name = "Alice"
    age = 30
    return name, age

name, age = get_name_and_age()

print(name)  # Output: "Alice"
print(age)  # Output: 30
```

Using tuples as dictionary keys:
Tuples can also be used as keys in dictionaries. This is because tuples are immutable and therefore can be hashed, while lists are not hashable and cannot be used as keys. For example:

```python
my_dict = {(1, 2): "value"}

print(my_dict[(1, 2)])  # Output: "value"
```

##Python dictionaries
In Python, a dictionary is a collection of key-value pairs, where each key is associated with a value. Dictionaries are unordered and mutable, meaning you can add, remove, or modify items after creation.

Dictionaries are created using curly braces {} or the dict() function, with each key-value pair separated by a colon : and each pair separated by a comma ,. For example:

```python
my_dict = {"key1": "value1", "key2": "value2", "key3": "value3"}

```
### Using Python dictionaries

Accessing values in a dictionary: 
To access a value in a dictionary, you can use the key associated with that value. For example:

```python
my_dict = {"name": "Alice", "age": 30}

print(my_dict["name"])  # Output: "Alice"
print(my_dict["age"])  # Output: 30

```

If the key does not exist in the dictionary, a KeyError will be raised. You can also use the get() method to retrieve a value, which will return None if the key does not exist, or a default value if specified. For example:

```python
my_dict = {"name": "Alice", "age": 30}

print(my_dict.get("name"))  # Output: "Alice"
print(my_dict.get("height"))  # Output: None
print(my_dict.get("height", 160))  # Output: 160

```

**Adding and modifying items in a dictionary**
To add an item to a dictionary, you can simply assign a new key-value pair to the dictionary. For example:

```python
my_dict = {"name": "Alice", "age": 30}

my_dict["height"] = 160

print(my_dict)  # Output: {"name": "Alice", "age": 30, "height": 160}

```

To modify an item in a dictionary, you can use the key associated with that item. For example:

```python
my_dict = {"name": "Alice", "age": 30}

my_dict["height"] = 160

print(my_dict)  # Output: {"name": "Alice", "age": 30, "height": 160}

```

**Removing items from a dictionary**
To remove an item from a dictionary, you can use the del keyword followed by the key associated with that item. For example:

```python
my_dict = {"name": "Alice", "age": 30}

del my_dict["age"]

print(my_dict)  # Output: {"name": "Alice"}

```


**Looping through a dictionary**
To loop through a dictionary, you can use a for loop with the items() method, which returns a list of key-value pairs. For example:

```python
my_dict = {"name": "Alice", "age": 30}

for key, value in my_dict.items():
    print(key, value)
    
# Output:
# name Alice
# age 30

```

Checking if a key exists in a dictionary
To check if a key exists in a dictionary, you can use the in keyword. For example:


```python
my_dict = {"name": "Alice", "age": 30}

if "name" in my_dict:
    print("Name exists in dictionary")

```
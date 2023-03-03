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
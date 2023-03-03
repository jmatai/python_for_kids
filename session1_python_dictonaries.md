# Python Dictionary 

A dictionary in Python is a collection of key-value pairs, where each key is associated with a value. Dictionaries are written in curly brackets {}, with each key-value pair separated by a colon :. Here's an example of a simple dictionary:

```python
my_dict = {"apple": 2, "banana": 3, "orange": 1}

```

In this example, the keys are strings ("apple", "banana", and "orange") and the values are integers (2, 3, and 1). You can access the values in the dictionary by specifying the corresponding key:

```python
print(my_dict["apple"])  # Output: 2
```

If you try to access a key that doesn't exist in the dictionary, you will get a KeyError:


```python
print(my_dict["pear"])  # Output: KeyError: 'pear'

```

You can also add, modify, and delete key-value pairs in a dictionary. Here's an example of adding a new key-value pair:
```python
my_dict["pear"] = 4
print(my_dict)  # Output: {"apple": 2, "banana": 3, "orange": 1, "pear": 4}

```

Here's an example of modifying an existing key-value pair:

```python
my_dict["banana"] = 5
print(my_dict)  # Output: {"apple": 2, "banana": 5, "orange": 1, "pear": 4}

```

And here's an example of deleting a key-value pair:
```python
del my_dict["orange"]
print(my_dict)  # Output: {"apple": 2, "banana": 5, "pear": 4}
```

You can also use loops to iterate over the keys and values in a dictionary. Here's an example:
```python
for key, value in my_dict.items():
    print(key, value)
```
This will output followings 

```python
apple 2
banana 5
pear 4
```


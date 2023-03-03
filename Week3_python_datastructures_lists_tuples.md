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

# Hashtable and Recurison 

## Hashtable and its deisgn 

A hashtable is a data structure that allows efficient insertion, deletion, and lookup of **key-value pairs**. It works by using a hash function to map each key to an index in an array, where the corresponding value is stored. When inserting or looking up a key-value pair, the hash function is applied to the key to determine the index in the array where the value is stored.

In python, dictionary datastructure ({}) is an implementation of hashtable. 

Hashtable is used in almost every field of computer science ranging from machine learning, computer networks to database indexing. 

**In this assignment, you have two tasks in hashtable (and one optional task for recursion -- see below).**
1) Read and about python dictionary from here: https://www.freecodecamp.org/news/python-dictionaries-detailed-visual-introduction/
2) Design and implement a hashtable class as follows: 

Hashtable is a class with following methods. 

**Insert(key, value):**
Inserts a key-value pair into the hashtable. The key is hashed to determine its index in the hashtable, and the key-value pair is inserted at the corresponding index. If there are collisions (i.e. if two keys hash to the same index), the key-value pairs are stored in a linked list at that index.
The time complexity of insert is O(1) on average, assuming a good hash function that evenly distributes keys across the hashtable. In the worst case (i.e. if all keys hash to the same index), the time complexity is O(n), where n is the number of keys in the hashtable.

**Delete(key):**
Deletes the key-value pair with the specified key from the hashtable. The key is hashed to determine its index in the hashtable, and the linked list at that index is searched to find the node containing the key-value pair. If found, the node is removed from the linked list.
The time complexity of delete is O(1) on average, assuming a good hash function and a reasonably sized linked list at each index. In the worst case (i.e. if all keys hash to the same index and are stored in a long linked list), the time complexity is O(n), where n is the length of the linked list at the index.

**Lookup(key):**
Returns the value associated with the specified key, if it exists in the hashtable. The key is hashed to determine its index in the hashtable, and the linked list at that index is searched to find the node containing the key-value pair. If found, the value associated with the key is returned.
The time complexity of lookup is O(1) on average, assuming a good hash function and a reasonably sized linked list at each index. In the worst case (i.e. if all keys hash to the same index and are stored in a long linked list), the time complexity is O(n), where n is the length of the linked list at the index.

Optional, you can have following method which resizes the hashtable. 

**Resize():**
Resizes the hashtable by creating a new, larger array and rehashing all the key-value pairs from the old array into the new array. Resizing is necessary when the number of key-value pairs in the hashtable exceeds a certain threshold, typically 75% of the hashtable's capacity.
The time complexity of resizing is O(n), where n is the number of key-value pairs in the hashtable, since every key-value pair must be rehashed and inserted into the new array. However, since resizing is infrequent and amortized over multiple insertions and deletions, the average time complexity of operations on a hashtable is still O(1).


Feel free to use following and other resources: 
- https://www.freecodecamp.org/news/what-is-hashing/
- https://www.educative.io/answers/what-is-a-hash-table
- https://www.educative.io/courses/data-structures-coding-interviews-python/B8ODKWQVq02


Submission:
Please push your code into your repo before our next meeting.  

## Recurision 

Recursion is a programming technique where a function calls itself to solve a problem or perform a computation. Recursion can be used to simplify complex problems by breaking them down into smaller sub-problems that can be solved recursively.


**Base case:** The function must have a base case that can be solved without recursion. The base case should be a simple problem that can be solved directly, without calling the function recursively. When the function reaches the base case, it should stop calling itself and return a value.

**Recursive case:** The function must have a recursive case that involves calling itself with a smaller sub-problem. The sub-problem should be simpler than the original problem, and it should eventually lead to the base case. The function should use the result of the recursive call to solve the original problem.

These conditions ensure that the recursive function will eventually terminate and not lead to an infinite loop. The base case provides the stopping condition, while the recursive case breaks the problem down into smaller sub-problems that can be solved using the same function.

Optional: Design and implement a function that finds the n factorial of a given number.

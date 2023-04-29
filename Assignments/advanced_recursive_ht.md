## Assignment : Recursion and HT 
1) Read abour recursion: https://www.educative.io/blog/recursion
2) Complete the assignment that find the determinant of matrix 

### Part 1: Find the determinant of a matrix 

Here is a template code for python sobel edge detection 
This is question 4 from: https://github.com/jmatai/python_for_kids/blob/main/session7_python_questions_linear_algebra%20-%20Copy.md 

Here, we provide a pseduo code for finding the determinant of a matrix using recurision. Use this pseduo code as an algorithm, 
and implement the determinant and smaller_matrix function in python. 

```python
function smaller_matrix(original_matrix, row, column):
    # Create a smaller matrix by deleting the specified row and column
    small_matrix = original_matrix with row deleted
    small_matrix = small_matrix with column deleted
    return small_matrix

function determinant(matrix):
    if matrix is not square:
        print an error message
        return None
    else if matrix is 2x2:
        calculate the determinant using the formula for a 2x2 matrix
        return the determinant
    else:
        answer = 0
        for each element in the first row of the matrix:
            calculate the cofactor by multiplying the element with the determinant of the smaller matrix
            - Set the sign of the cofactor as (-1)^(row+column) where row is 0 and column is the index of the current element
            - Obtain the smaller matrix by calling the smaller_matrix function with the current element's indices
            - Calculate the determinant of the smaller matrix by recursively calling the determinant function
            - Multiply the element with the sign and the determinant of the smaller matrix to get the cofactor
            update the answer by adding the cofactor
        return the accumulated answer, which represents the determinant of the input matrix
```
You can use numpy to create 2D matrix, and you can also use the numpy delete method for creating small_matrix (smaller_matrix function).
Here is how I test the code. 

```python
np.random.seed(1)
matrix = np.random.rand(10, 10)

# Testing determinant function. 
a = determinant(matrix)

# Running the numpy det function so that we can compare our results  
np_det = np.linalg.det(matrix)

print(a)
print(np_det)

```


### Part 2: Hash table 

Implement a complete HT in python. Here you can find how to do resize in HT with python [resize in HT] (https://realpython.com/python-hash-table/#let-the-hash-table-resize-automatically)

More helpful resources are here: 
- Read about [Dicontaries in python](https://stackoverflow.com/questions/327311/how-are-pythons-built-in-dictionaries-implemented).
- Read about [More on HT in python](https://stackoverflow.com/questions/2061222/what-is-the-true-difference-between-a-dictionary-and-a-hash-table/2061406).
- Read about [HT with python more] (https://medium.com/@erikbatista42/an-introduction-to-hash-tables-with-python-817772cad688)
 


 


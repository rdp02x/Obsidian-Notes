### MCQs

1. Which of the following is the fundamental package for numerical computing in Python?  
   - A) SciPy  
   - **B) NumPy**  
   - C) Pandas  
   - D) Matplotlib  

2. What is the primary object type in NumPy that can store elements of a single data type?  
   - A) List  
   - B) Tuple  
   - **C) Array**  
   - D) Dictionary  

3. Which NumPy function is used to create an array filled with zeros?  
   - A) numpy.zeroes()  
   - **B) numpy.zeros()**  
   - C) numpy.zeros_array()  
   - D) numpy.create_zeros()  

4. In NumPy, how can you create an array of evenly spaced values over a specified interval?  
   - **A) numpy.linspace()**  
   - B) numpy.arange()  
   - C) numpy.range()  
   - D) numpy.evenly()  

5. Which of the following methods returns the number of elements along a specific axis?  
   - A) numpy.shape()  
   - **B) numpy.size()**  
   - C) numpy.dimensions()  
   - D) numpy.count()  

6. What function is used in NumPy to reshape an array?  
   - **A) numpy.reshape()**  
   - B) numpy.restructure()  
   - C) numpy.rearrange()  
   - D) numpy.reform()  

7. Which of the following operations in NumPy performs matrix multiplication?  
   - A) numpy.dot()  
   - B) numpy.multiply()  
   - **C) numpy.matmul()**  
   - D) numpy.prod()  

8. How can you concatenate two arrays arr1 and arr2 along axis 1 in NumPy?  
   - A) numpy.concatenate(arr1, arr2, axis=1)  
   - B) numpy.concat(arr1, arr2, axis=1)  
   - C) numpy.join(arr1, arr2, axis=1)  
   - **D) numpy.hstack((arr1, arr2))**  

9. Which NumPy function returns the indices that would sort an array?  
   - A) numpy.sort_indices()  
   - **B) numpy.argsort()**  
   - C) numpy.sort()  
   - D) numpy.index_sort()  

10. What is the function to calculate the mean of elements in a NumPy array?  
    - **A) numpy.mean()**  
    - B) numpy.average()  
    - C) numpy.mean_array()  
    - D) numpy.get_mean()  

11. How can you transpose a NumPy array arr?  
    - A) arr.transpose()  
    - **B) numpy.transpose(arr)**  
    - C) numpy.trans(arr)  
    - D) numpy.transpose_array(arr)  

12. Which function is used to find the unique elements of an array in NumPy?  
    - **A) numpy.unique()**  
    - B) numpy.uniq()  
    - C) numpy.distinct()  
    - D) numpy.find_unique()  

13. How do you compute the element-wise square root of a NumPy array arr?  
    - **A) numpy.sqrt(arr)**  
    - B) arr.sqrt()  
    - C) numpy.square_root(arr)  
    - D) numpy.sqrt_array(arr)  

14. What does the NumPy function numpy.where() do?  
    - **A) Finds the indices of elements that satisfy a condition**  
    - B) Returns the elements that satisfy a condition  
    - C) Counts the number of elements that satisfy a condition  
    - D) Splits the array based on a condition  

15. How can you extract the diagonal elements of a NumPy array arr?  
    - A) arr.diagonal()  
    - **B) numpy.diagonal(arr)**  
    - C) numpy.get_diagonal(arr)  
    - D) numpy.extract_diagonal(arr)  

16. Which function is used to find the maximum element along a specified axis in NumPy?  
    - A) numpy.max()  
    - B) numpy.maximum()  
    - **C) numpy.amax()**  
    - D) numpy.max_element()  

17. What is the purpose of NumPy's broadcasting?  
    - A) Changing the data type of elements in an array  
    - **B) Performing element-wise operations on arrays of different shapes**  
    - C) Reordering the elements of an array  
    - D) Sorting the elements of an array  

18. How can you convert a Python list my_list to a NumPy array?  
    - A) numpy.convert(my_list)  
    - **B) numpy.array(my_list)**  
    - C) numpy.to_array(my_list)  
    - D) numpy.make_array(my_list)  

19. Which function is used to save a NumPy array to a binary file?  
    - **A) numpy.save()**  
    - B) numpy.save_array()  
    - C) numpy.save_bin()  
    - D) numpy.export()  

20. How can you load a NumPy array from a binary file?  
    - A) numpy.read()  
    - B) numpy.load_file()  
    - **C) numpy.load()**  
    - D) numpy.load_bin()  

21. What is the correct way to calculate the dot product of two arrays a and b in NumPy?  
    - **A) numpy.dot(a, b)**  
    - B) a.dot(b)  
    - C) numpy.dot_product(a, b)  
    - D) numpy.multiply(a, b)  

22. Which function is used to generate random numbers from a uniform distribution in NumPy?  
    - A) numpy.random.uniform()  
    - B) numpy.uniform()  
    - C) numpy.random.random()  
    - **D) numpy.random.rand()**  

23. How can you perform element-wise addition of two NumPy arrays arr1 and arr2?  
    - **A) arr1 + arr2**  
    - B) numpy.add(arr1, arr2)  
    - C) numpy.element_add(arr1, arr2)  
    - D) numpy.addition(arr1, arr2)  

24. Which function is used to find the indices of the maximum and minimum elements of a NumPy array?  
    - A) numpy.maxmin()  
    - B) numpy.argminmax()  
    - **C) numpy.argmin(), numpy.argmax()**  
    - D) numpy.indexminmax()  

25. What is the purpose of the NumPy function numpy.meshgrid()?  
    - A) Converts arrays into a mesh-like grid  
    - B) Reshapes arrays into a grid format  
    - **C) Generates coordinate matrices from coordinate vectors**  
    - D) Interpolates arrays into a grid structure

### All Functions

##### Array Creation Functions:
1. **`np.array()`**: Creates an array from a Python list or iterable.
2. **`np.zeros()`**: Creates an array filled with zeros.
3. **`np.ones()`**: Creates an array filled with ones.
4. **`np.empty()`**: Creates an uninitialized array (values are arbitrary).
5. **`np.full()`**: Creates an array filled with a specified value.
6. **`np.arange()`**: Creates an array with evenly spaced values within a specified interval.
7. **`np.linspace()`**: Creates an array with evenly spaced values over a specified interval.
8. **`np.eye()`**: Creates a 2D identity matrix with ones on the diagonal and zeros elsewhere.
9. **`np.identity()`**: Creates an identity matrix.
10. **`np.random.rand()`**: Generates an array of random numbers from a uniform distribution over [0, 1].
11. **`np.random.randn()`**: Generates an array of random numbers from a standard normal distribution.
12. **`np.random.randint()`**: Generates random integers within a specified range.
13. **`np.random.random()`**: Generates random floats from a uniform distribution over [0, 1].
14. **`np.random.choice()`**: Generates a random sample from a given 1-D array.
15. **`np.random.shuffle()`**: Shuffles the contents of an array in-place.
##### Array Manipulation Functions:
1. **`np.reshape()`**: Reshapes an array into a specified shape.
2. **`np.ravel()`**: Flattens an array into a 1-D array.
3. **`np.transpose()` or `.T`**: Transposes an array, swapping its axes.
4. **`np.hstack()`**: Stacks arrays horizontally (along columns).
5. **`np.vstack()`**: Stacks arrays vertically (along rows).
6. **`np.concatenate()`**: Concatenates arrays along a specified axis.
7. **`np.split()`**: Splits an array into multiple sub-arrays.
8. **`np.append()`**: Appends values to the end of an array.
9. **`np.insert()`**: Inserts values into an array at a specified index.
10. **`np.delete()`**: Deletes elements from an array at a specified index.
##### Mathematical Functions:
1. **`np.add()`**: Adds corresponding elements of two arrays.
2. **`np.subtract()`**: Subtracts elements of the second array from the first.
3. **`np.multiply()`**: Multiplies corresponding elements of two arrays.
4. **`np.divide()`**: Divides elements of the first array by elements of the second array.
5. **`np.power()`**: Raises elements of the first array to powers given in the second array.
6. **`np.exp()`**: Calculates the exponential of all elements in the input array.
7. **`np.log()`**: Computes the natural logarithm of each element in the array.
8. **`np.sqrt()`**: Computes the square root of each element in the array.
##### Statistical Functions:
1. **`np.mean()`**: Computes the arithmetic mean along a specified axis.
2. **`np.median()`**: Computes the median along a specified axis.
3. **`np.std()`**: Computes the standard deviation along a specified axis.
4. **`np.var()`**: Computes the variance along a specified axis.
5. **`np.sum()`**: Sums array elements over a specified axis.
6. **`np.min()`**: Returns the minimum value along a specified axis.
7. **`np.max()`**: Returns the maximum value along a specified axis.
8. **`np.argmin()`**: Returns the indices of the minimum values along an axis.
9. **`np.argmax()`**: Returns the indices of the maximum values along an axis.
##### Linear Algebra Functions:
1. **`np.dot()`**: Computes the dot product of two arrays.
2. **`np.matmul()`**: Performs matrix multiplication of two arrays.
3. **`np.linalg.inv()`**: Computes the multiplicative inverse of a matrix.
4. **`np.linalg.det()`**: Computes the determinant of a matrix.
5. **`np.linalg.eig()`**: Computes the eigenvalues and eigenvectors of a square matrix.
6. **`np.linalg.svd()`**: Performs Singular Value Decomposition (SVD) of a matrix.
##### Sorting, Searching, and Counting Functions:
1. **`np.sort()`**: Sorts elements of an array along a specified axis.
2. **`np.argsort()`**: Returns the indices that would sort an array.
3. **`np.searchsorted()`**: Finds indices where elements should be inserted to maintain order.
4. **`np.count_nonzero()`**: Counts the number of non-zero elements in the array.
5. **`np.unique()`**: Finds the unique elements of an array.
##### File Input and Output Functions:
1. **`np.load()`**: Loads arrays or pickled objects from `.npy`, `.npz`, or pickled files.
2. **`np.save()`**: Saves an array to a binary file in `.npy` format.
3. **`np.savetxt()`**: Saves an array to a text file.
4. **`np.loadtxt()`**: Loads data from a text file.
##### Random Number Generation Functions:
1. **`np.random.seed()`**: Seeds the random number generator.
2. **`np.random.rand()`**: Generates random numbers from a uniform distribution over [0, 1].
3. **`np.random.randn()`**: Generates random numbers from a standard normal distribution.
4. **`np.random.randint()`**: Generates random integers within a specified range.

### Questions

#### What is NumPy?
- **NumPy (Numerical Python)**: A powerful Python library for numerical computations.
- Provides support for large multidimensional arrays and matrices.
- Includes mathematical functions to operate on these arrays efficiently.

#### Why should we use NumPy?
- **Efficiency**: NumPy arrays are faster and more memory-efficient than Python lists.
- **Performance**: Allows vectorized operations, avoiding slow loops.
- **Mathematical Functions**: Includes a wide range of functions for numerical tasks.

#### How do you create a NumPy array?
- Use **`np.array()`** to create an array from a Python list or tuple.
- Example:
  ```python
  import numpy as np
  arr = np.array([1, 2, 3, 4, 5])
  ```

#### Advantages of using NumPy arrays over Python lists:
- **Faster** and more memory-efficient for numerical computations.
- **Vectorized operations**: Perform operations on entire arrays at once, eliminating loops.
- **Broad functionality**: Supports various mathematical functions for arrays.

#### How do you perform element-wise operations in NumPy?
- Use arithmetic operators **(`+`, `-`, `*`, `/`)** for element-wise operations.
- Apply mathematical functions like **`np.sin()`**, **`np.exp()`**, etc.
- Example:
  ```python
  arr1 = np.array([1, 2, 3])
  arr2 = np.array([4, 5, 6])
  result = arr1 + arr2  # Result: [5, 7, 9]
  ```

#### Explain broadcasting in NumPy:
- **Broadcasting**: Allows operations on arrays of different shapes.
- Stretches smaller arrays to match the shape of larger ones.
- Enables operations on arrays that would otherwise be incompatible.

#### Commonly used functions in NumPy:
- **Array Creation**: `np.array()`, `np.zeros()`, `np.ones()`, `np.arange()`, `np.linspace()`
- **Array Manipulation**: `np.reshape()`, `np.transpose()`, `np.concatenate()`, `np.split()`
- **Mathematical Functions**: `np.sum()`, `np.mean()`, `np.std()`, `np.min()`, `np.max()`, `np.dot()`, `np.linalg.inv()`
- **Statistical Functions**: `np.histogram()`, `np.corrcoef()`, `np.cov()`
- **Random Number Generation**: `np.random.rand()`, `np.random.randn()`, `np.random.randint()`

#### How do you save and load NumPy arrays from files?
- **Save** arrays: `np.save()` for binary files, `np.savetxt()` for text files.
- **Load** arrays: `np.load()` for binary files, `np.loadtxt()` for text files.

#### Difference between `np.array` and Python's `array.array`:
- **`np.array`**: Supports multidimensional arrays and a wide range of functions.
- **`array.array`**: Limited to one-dimensional arrays of a single data type.

#### How can NumPy be integrated with other Python libraries like Pandas and Matplotlib?
- **Pandas**: NumPy arrays can be used as data structures in DataFrames and Series.
- **Matplotlib**: Accepts NumPy arrays as inputs for creating plots and visualizations.

### Images

#### NumPy Basics:
- **NumPy** is the core library for scientific computing in Python, providing a high-performance multidimensional array object and tools for working with these arrays.
- **Import Convention:**
  - `import numpy as np`
#### NumPy Arrays:
- **1D Array:** A single-dimensional array, like `[1, 2, 3]`.
- **2D Array:** A two-dimensional array (matrix) with rows and columns.
- **3D Array:** A three-dimensional array, with three axes (axis 0, axis 1, and axis 2).
#### Creating Arrays:
- **Basic Array Creation:**
  - `a = np.array([1, 2, 3])` creates a 1D array.
  - `b = np.array([(1.5, 2.3), (4.5, 6)], dtype=float)` creates a 2D array with specified `dtype`.
  - `c = np.array([[(1.5, 2.3), (4.5, 6)], [(3, 2, 1), (4, 5, 6)]], dtype=float)` creates a 3D array.
#### Initial Placeholders:
- `np.zeros((3,4))`: Creates an array of zeros with the shape (3, 4).
- `np.ones((2,3,4)`, `dtype=np.int16)`: Creates an array of ones with the shape (2, 3, 4) and data type int16.
- `np.arange(10,25,5)`: Creates an array with values spaced by 5 from 10 to 25.
- `np.linspace(0,2,9)`: Creates an array of 9 evenly spaced values from 0 to 2.
- `np.full((2, 2), 7)`: Creates a constant array filled with 7.
- `np.eye(2)`: Creates a 2x2 identity matrix.
- `np.random.random((2, 2))`: Creates an array filled with random values.
- `np.empty((3, 2))`: Creates an empty array with the shape (3, 2).
#### Inspecting Your Array:
- `a.shape`: Returns the dimensions of the array.
- `len(a)`: Returns the length of the array.
- `b.ndim`: Returns the number of dimensions in the array.
- `e.size`: Returns the number of elements in the array.
- `b.dtype`: Returns the data type of the array elements.
- `b.dtype.name`: Returns the name of the data type.
- `b.astype(int)`: Converts the array to a different type, here converting it to integers.

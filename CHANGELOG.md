## [0.0.1] - 2022-10-29
# Changelog

### Added

- Added a Python class `Vector` for performing vector operations in 2D and 3D space.
- Implemented methods for vector manipulation, calculations, and file I/O.

### Methods

- `__init__(self, data: list[int|float])`: Initialize a vector with the given data.
- `__setitem__(self, key, value: int | float)`: Set the value at the specified index in the vector.
- `__getitem__(self, key)`: Get the value at the specified index in the vector.
- `__iter__(self)`: Iterate over the elements of the vector.
- `__len__(self)`: Get the length of the vector.
- `__str__(self, mode='default')`: Get a string representation of the vector.
- `__sum__(self)`: Calculate the sum of the vector's elements.
- `__min__(self)`: Get the minimum value in the vector.
- `__max__(self)`: Get the maximum value in the vector.
- `__eq__(self, other)`: Check if two vectors are equal element-wise.
- `__ne__(self, other)`: Check if two vectors are not equal element-wise.
- `__mul__(self, other: 'Vector | int | float')`: Multiply the vector by another vector, an integer, or a float.
- `__rmul__(self, other: int | float)`: Multiply the vector by an integer or float.
- `__add__(self, other: 'Vector')`: Add two vectors element-wise.
- `__sub__(self, other: 'Vector')`: Subtract two vectors element-wise.
- `__truediv__(self, other: int | float)`: Divide the vector by an integer or float.
- `__floordiv__(self, other: int | float)`: Perform integer division on the vector by an integer or float.
- `__mod__(self, other: int | float)`: Calculate the modulo of the vector by an integer or float.
- `extend(self, iterable: Iterable[int | float])`: Extend the vector with elements from an iterable.
- `append(self, item: int | float)`: Append an element to the end of the vector.
- `clear(self)`: Remove all elements from the vector.
- `reverse(self)`: Reverse the order of elements in the vector.
- `scalar(self, other: 'Vector')`: Calculate the scalar product of two vectors.
- `cross(self, other: 'Vector')`: Calculate the cross product of two 3D vectors.
- `norm(self)`: Calculate the magnitude (norm) of the vector.
- `nomralize(self)`: Normalize the vector to have a magnitude of 1.
- `rotate_2d(self, angle_degrees: float)`: Rotate the 2D vector by a specified angle in degrees.
- `rotate_3d(self, angle_degrees: float, axis: str='x')`: Rotate the 3D vector by a specified angle in degrees around a specified axis.
- `rotate_nd(self, angle_degrees: float, axis_indices: list[int])`: Rotate the vector in N dimensions by a specified angle in degrees around specified axes.
- `angle_between_vectors(self, other: 'Vector')`: Calculate the angle in degrees between two vectors.
- `vector_projection(self, other: 'Vector')`: Calculate the vector projection of the vector onto another vector.
- `to_polar(self)`: Convert a 2D vector to polar coordinates (r, theta).
- `to_spherical(self)`: Convert a 3D vector to spherical coordinates (r, theta, phi).
- `to_conical(self)`: Convert a 3D vector to conical coordinates (r, theta, phi).
- `are_orthogonal(self, other: 'Vector')`: Check if two vectors are orthogonal (perpendicular).
- `are_parallel(self, other)`: Check if two vectors are parallel.
- `sum(self)`: Calculate the sum of the vector's elements.
- `mean(self)`: Calculate the mean of the vector's elements.
- `min(self)`: Get the minimum value in the vector.
- `max(self)`: Get the maximum value in the vector.
- `dim(self)`: Get the dimension of the vector.
- `sort(self)`: Sort the elements of the vector in ascending order.
- `_partition(self, left, right)`: Helper method for sorting.
- `draw2d(vectors, color)`: Visualize 2D vectors with optional colors.
- `draw3d(vectors, color)`: Visualize 3D vectors with optional colors.

### Functions

- `randvec(length, lower, upper)`: Generate a random Vector of specified length with elements between lower and upper values.
- `zeros(num)`: Create a Vector filled with zeros.
- `nvec(scal, num)`: Create a Vector with a specified scalar repeated a number of times.
- `degrees_to_radians(degrees)`: Convert degrees to radians.
- `radians_to_degrees(radians)`: Convert radians to degrees.

### File I/O

- `save_to_file(self, filename='vector.pkl')`: Save the vector to a binary file.
- `load_from_file(cls, filename: str) -> 'Vector'`: Load a vector from a binary file.
- `save_vectors_to_file(cls, vectors: list[Vector], filename: str)`: Save a list of vectors to a binary file.
- `load_vectors_from_file(cls, filename: str) -> list['Vector']`: Load a list of vectors from a binary file.

### Error Handling

- Introduced custom exceptions such as `VectorDimensionMismatchError`, `VectorLengthMismatchError`, `VectorOutOfRangeError`, and `VectorError` for better error handling.

### Examples

- Provided examples of how to use the `Vector` class for various vector operations in 2D and 3D space.


### Custom Exceptions

- `VectorError(Exception)`: Base class for exceptions related to vectors.
  - Custom exception class for vector-related errors.
- `VectorLengthMismatchError(VectorError)`: Exception raised when vector lengths do not match.
  - Raised when attempting operations on vectors with different lengths.
- `VectorDimensionMismatchError(VectorError)`: Exception raised when vector dimensions do not match.
  - Raised when trying to perform operations on vectors with different dimensions.
- `VectorOutOfRangeError(VectorError)`: Exception raised when accessing an index out of range.
  - Raised when trying to access an index outside the valid range of the vector.

### Error Messages

- Custom error messages for the exceptions are defined:
  - `OUTOFRANGEERR_MSG`: "Index {index} is out of the valid range (0-{out_length})"
  - `DIMMISMATCHERR_MSG`: "Expected dimension {expected_dimension}, but received dimension {actual_dimension}"
  - `LENGTHMISMATCHERR_MSG`: "Vector lengths do not match"


### Documentation

- Updated the class documentation with method descriptions and usage examples.

### Other

- Removed unused import statements for optimization.

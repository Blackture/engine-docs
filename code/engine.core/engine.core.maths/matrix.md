---
description: Engine.Core.Maths
---

# Matrix Class

## Class Matrix

The `Matrix` class represents a matrix with floating point values. The class provides functionality to perform operations on matrices such as addition, subtraction, multiplication, and indexing.

### Properties

* `Values`: A two dimensional list of floating point values that represent the elements of the matrix.
* `RowCount`: An integer that represents the number of rows in the matrix.
* `ColumnCount`: An integer that represents the number of columns in the matrix.

### Indexer

A two dimensional indexer is provided that allows to access and modify elements of the matrix using the row and column indices.

### Constructors

* `Matrix(int rowCount, int columnCount)`: Constructs a matrix with the specified number of rows and columns.
* `Matrix(List<List<float>> values)`: Constructs a matrix from a given two dimensional list of floating point values.

### Operators

* `+`: Adds two matrices. Throws an exception if the dimensions of the matrices are different.
* `-`: Subtracts two matrices. Throws an exception if the dimensions of the matrices are different.
* `*`: Multiplies two matrices or a matrix and a scalar. Throws an exception if the number of columns of the first matrix is not equal to the number of rows of the second matrix.

### Methods

* `GetRow(int index)`: Returns the specified row of the matrix. If the index is outside the range of rows, returns `null`.
* `GetColumn(int index)`: Returns the specified column of the matrix. If the index is outside the range of columns, returns `null`.
* `ConvertTo(List<List<float>> matrix)`: Converts a given two dimensional list of floating point values to a `Matrix` object.

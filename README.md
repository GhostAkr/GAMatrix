# GAMatrix
Library that defines class describing matrices
-----------------------------------------------
Each *Matrix* object is a container that consists of *data* (contains values of *Matrix*), *rows* (contains number of rows in *Matrix*), *cols* (contains number of columns in *Matrix*). GAMatrix uses custom variable *type* for calculating with different accuracy. It can be changed for any C++ float type. Avaliable functions for operating with *Matrix* are listed below.
## Constructors
* `Matrix(size_t _rows, size_t _cols)` – create *Matrix* whith *_rows* rows and *_cols* columns filled with zeros.

## Access methods
* `void matrixSet(type** _data, size_t _rows, size_t _cols)` – rewrite current *Matrix* with parameters listed in arguments;
* `type** matrixGet() const` – return *data* of current *Matrix*;
* `void matrixPrint() const` – print current *Matrix* on screen;
* `size_t rowsGet() const` – return number of rows in current *Matrix*;
* `size_t colsGet() const` – return number of columns in current *Matrix*;
* `void rowsSet(size_t _rows)` – set *rows* in current *Matrix* to *_rows* (that don't modify *data*);
* `void colsSet(size_t _cols)` – set *cols* in current *Matrix* to *_cols* (that don't modify *data*);

## Import data
* void readMatrixFromFile(string _pathToFile) – import *Matrix* from file.
Example of file structure that valid for import:

3 3

1 2 3

4 5 6

7 8 9

(In first line need to write number of rows and number of columns)

## Operations methods
(Note that static methods requires `Matrix::` when calling it);
* `static Matrix* matrixSum(const Matrix* _matrix1, const Matrix* _matrix2)` – sum of 2 *Matrix*;
* `static Matrix* matrixComp(const Matrix* _matrix1, const Matrix* _matrix2)` – composition of 2 *Matrix*;
* `static Matrix* matrixDiff(const Matrix* _matrix1, const Matrix* _matrix2)` – difference of 2 *Matrix*;
* `static Matrix* matrixConstComp(const Matrix* _matrix, const type _const)` – multiplying *Matrix* by constant;
* `static Matrix* getCopy(const Matrix* _matrix)` – return copy of *_matrix*;
* `void matrixRowsChange(int firstRow, int secondRow)` – swap rows in *Matrix* with numbers *firstRow* and *secondRow*;
* `void matrixTranspose` – transpose *Matrix*;

## Special matrices
* `void matrixNullSet(size_t _rows, size_t _cols)` – create *Matrix* consisting of zeros;
* `void matrixOneSet(size_t _rows, size_t _cols)` – create identity *Matrix*.

# matrix_stack_set

This function overwrites the current top of the matrix stack with the
specified matrix.

#### Syntax:

``` gml
matrix_stack_set(matrix);
```

|          |                                                                                                                           |                          |
|----------|---------------------------------------------------------------------------------------------------------------------------|--------------------------|
| Argument | Type                                                                                                                      | Description              |
| matrix   |  [Matrix Array](../../../../../GameMaker_Language/GML_Reference/Maths_And_Numbers/Matrix_Functions/Matrix_Functions)  | The matrix index to use. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
var m = matrix_build(x, y, 0, 0, 0, 0, 1, 1, 1); matrix_stack_set(m);
```

The above code will build a new matrix and store the resulting matrix
index in the variable "m" before replacing the top of the matrix stack
with it.

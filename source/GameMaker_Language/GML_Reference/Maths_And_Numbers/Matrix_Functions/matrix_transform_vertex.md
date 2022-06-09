# matrix_transform_vertex

This function transforms a vector by a matrix. You supply the transform
matrix ID (as returned by the function [ matrix build()
](matrix_build) ), as well as the x, y and z values for the vector
to transform. The function will return an
[array](../../../GML_Overview/Arrays) of 3 elements where:

-   array\[0\] = x
-   array\[1\] = y
-   array\[2\] = z.

#### Syntax:

``` gml
matrix_transform_vertex(matrix, x, y, z);
```

|          |                                                                                                                           |                                         |
|----------|---------------------------------------------------------------------------------------------------------------------------|-----------------------------------------|
| Argument | Type                                                                                                                      | Description                             |
| matrix   |  [Matrix Array](../../../../../GameMaker_Language/GML_Reference/Maths_And_Numbers/Matrix_Functions/Matrix_Functions)  | The matrix to use                       |
| x        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                    | The x component of the transform vector |
| y        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                    | The y component of the transform vector |
| z        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                    | The z component of the transform vector |

#### Returns:

``` gml
 Array

(3 elements)
```

#### Example:

``` gml
t_matrix = matrix_build(0, 0, 0, 0, 90, 0, 1, 2, 1); verts = matrix_transform_vertex(t_matrix, x, y, z);
```

The above code transforms the given values using the matrix stored in
the variable "t_matrix" and stores them in the array "verts".

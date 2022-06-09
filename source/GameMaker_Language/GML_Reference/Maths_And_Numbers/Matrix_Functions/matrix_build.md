# matrix_build

This function can be used to create your own custom matrix and will
return a matrix array, which should be stored in a variable for future
reference and use. It accepts 3-dimensional ( x, y, z ) translation,
rotation and scale values, and uses them to build a matrix array. The
matrix array contains 16 values in total, where the initial 4 elements
are ***row/column 1*** , the next 4 elements are ***row/column 2*** and
so on, as part of a [4x4 matrix](Matrix_Functions) . Whether the
array is ordered by rows or columns depends on the target platform, as
the graphics renderer used by a platform may use row-major or
column-major matrices. NOTE When you build a new matrix in this way, the
order of operation is YXZ.

#### Syntax:

``` gml
matrix_build(x, y, z, xrotation, yrotation, zrotation, xscale, yscale, zscale);
```

|           |                                                                         |                                                       |
|-----------|-------------------------------------------------------------------------|-------------------------------------------------------|
| Argument  | Type                                                                    | Description                                           |
| x         |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The x component of the translation vector.            |
| y         |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The y component of the translation vector.            |
| z         |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The z component of the translation vector.            |
| xrotation |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The angle to rotate around the x-axis (in degrees °). |
| yrotation |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The angle to rotate around the y-axis (in degrees °). |
| zrotation |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The angle to rotate around the z-axis (in degrees °). |
| xscale    |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The x scale amount.                                   |
| yscale    |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The y scale amount.                                   |
| zscale    |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The z scale amount.                                   |

#### Returns:

``` gml
 Matrix Array
```

#### Example:

``` gml
t_matrix = matrix_build(x, y, 0, 0, 90, 0, 1, 2, 1);
```

The above code will build a new matrix transform and store the resulting
matrix index in the variable "t_matrix".

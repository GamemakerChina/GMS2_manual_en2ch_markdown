# matrix_set

This function takes an [array](../../../GML_Overview/Arrays) of 16
values, corresponding to a given 4x4 matrix type, where elements \[0 -
3\] would be row 1, elements \[4 -7\] would be row 2, etc... (see the
image on the [main page](Matrix_Functions) ). You can create such a
matrix using the [ matrix_build() ](matrix_build) or [ matrix_get()
](matrix_get) functions or simply building the array yourself and
passing that into the function. The available matrix types are *view* ,
*projection* and *world* , for which you would use one of the following
constants:

|                     |                               |
|---------------------|-------------------------------|
| Constant            | Description                   |
|  matrix_view        | The current view matrix       |
|  matrix_projection  | The current projection matrix |
|  matrix_world       | The current world matrix      |

#### Syntax:

``` gml
matrix_set(type, matrix);
```

|          |                                                                                                                             |                                                                            |
|----------|-----------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| Argument | Type                                                                                                                        | Description                                                                |
| type     |  [Matrix Type Constant](../../../../../GameMaker_Language/GML_Reference/Maths_And_Numbers/Matrix_Functions/matrix_get)  | The type of matrix to get the values of (see the *constants* listed above) |
| matrix   |  [Matrix Array](../../../../../GameMaker_Language/GML_Reference/Maths_And_Numbers/Matrix_Functions/Matrix_Functions)    | The matrix data as an array                                                |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
matrix_set(matrix_world, m_array);
```

The above code will set the values of the current world matrix to those
stored in the array matrix "m_array".

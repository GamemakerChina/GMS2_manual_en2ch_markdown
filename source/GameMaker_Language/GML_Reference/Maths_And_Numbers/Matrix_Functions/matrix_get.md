# matrix_get

This function returns an [array](../../../GML_Overview/Arrays) of 16
values, corresponding to the given 4x4 matrix type, where row 1 is
elements \[0 - 3\], row 2 is elements \[4 -7\], etc... (see the image on
the [main page](Matrix_Functions) ). The available matrices are
*view* , *projection* and *world* , for which you would use one of the
following constants:

|                                                                                                                             |                               |
|-----------------------------------------------------------------------------------------------------------------------------|-------------------------------|
|  [Matrix Type Constant](../../../../../GameMaker_Language/GML_Reference/Maths_And_Numbers/Matrix_Functions/matrix_get)  |                               |
| Constant                                                                                                                    | Description                   |
|  matrix_view                                                                                                                | The current view matrix       |
|  matrix_projection                                                                                                          | The current projection matrix |
|  matrix_world                                                                                                               | The current world matrix      |

#### Syntax:

``` gml
matrix_get(type);
```

|          |                                                                                                                             |                                                              |
|----------|-----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| Argument | Type                                                                                                                        | Description                                                  |
| type     |  [Matrix Type Constant](../../../../../GameMaker_Language/GML_Reference/Maths_And_Numbers/Matrix_Functions/matrix_get)  | The type of matrix to get (see the *constants* listed above) |

#### Returns:

``` gml
 Matrix Array
```

#### Example:

``` gml
v_array = matrix_get(matrix_view);
```

The above code will get the values of the current view matrix and
populate the array "v_array" with them.

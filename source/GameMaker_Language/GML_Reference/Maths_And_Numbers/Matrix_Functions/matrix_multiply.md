# matrix_multiply

With this function you can multiply two matrix arrays together to create
a new transform matrix. The function will return the new matrix index
which should be stored in a variable for future use. **NOTE** : You
can't use a matrix constant as an argument with this function, so if you
wish to multiply the (for example) view matrix with a custom matrix that
you have built, you must first call [ matrix_get() ](matrix_get) and
assign the view matrix values to an array variable, then multiply it by
your custom matrix, and then set the chosen matrix (view, projection or
world).

#### Syntax:

``` gml
matrix_multiply(matrix1, matrix2);
```

|          |                                                                                                                           |                                 |
|----------|---------------------------------------------------------------------------------------------------------------------------|---------------------------------|
| Argument | Type                                                                                                                      | Description                     |
| matrix1  |  [Matrix Array](../../../../../GameMaker_Language/GML_Reference/Maths_And_Numbers/Matrix_Functions/Matrix_Functions)  | The first matrix index to use.  |
| matrix2  |  [Matrix Array](../../../../../GameMaker_Language/GML_Reference/Maths_And_Numbers/Matrix_Functions/Matrix_Functions)  | The second matrix index to use. |

#### Returns:

``` gml
 Matrix Array
```

#### Example:

``` gml
var v_matrix = matrix_get(matrix_view);
var new_matrix = matrix_multiply(v_matrix, my_matrix);
matrix_set(matrix_view, new_matrix);
```

The above code will get the current view matrix, then multiply that with
a custom matrix and then use the resulting matrix index to set the view
matrix again.

# matrix_build_projection_perspective_fov

This function builds a perspective projection matrix matrix based on
field of view, using the specified parameters listed below.

#### Syntax:

``` gml
matrix_build_projection_perspective_fov(fov_y, aspect, znear, zfar);
```

|          |                                                                         |                                        |
|----------|-------------------------------------------------------------------------|----------------------------------------|
| Argument | Type                                                                    | Description                            |
| fov      |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The angle of the field of view.        |
| aspect   |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The aspect ratio of the field of view. |
| znear    |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The near clipping plane.               |
| zfar     |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The far clipping plane.                |

#### Returns:

``` gml
 Matrix Array
```

#### Example:

``` gml
projmat = matrix_build_projection_perspective_fov(60, 320/240, 1.0, 32000.0);
camera_set_proj_mat(view_camera[0], projmat);
```

The above code creates a field of view projection matrix which is then
stored in a variable. This matrix is then used to set up the camera
assigned to view port\[0\].

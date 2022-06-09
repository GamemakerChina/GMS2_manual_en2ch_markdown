# matrix_build_lookat

This function builds a "look-at" (view) matrix based on the specified
parameters listed below. Since this function modifies the view matrix
and not the projection matrix, you should first initialize the
projection matrix using the other matrix function [
matrix_build_projection_perspective()
](matrix_build_projection_perspective) , then use this function to
move the view camera around within the projection. To set the view you
first need to define the position you look *from* , which is indicated
by the parameters (xfrom, yfrom, zfrom). Next you must specify the
direction you look *at* and this is done by giving a second point to
look towards with the arguments (xto, yto, zto). Finally, you can still
rotate the camera around the line from the viewpoint to the looking
point, and to specify this we must give an "up" vector - the direction
that is upwards in the camera. This is given by the last three arguments
(xup, yup, zup).

#### Syntax:

``` gml
matrix_build_lookat(xfrom, yfrom, zfrom, xto, yto, zto, xup, yup, zup);
```

|          |                                                                         |                                                |
|----------|-------------------------------------------------------------------------|------------------------------------------------|
| Argument | Type                                                                    | Description                                    |
| xfrom    |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The x coordinate of the position to look from. |
| yfrom    |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The y coordinate of the position to look from. |
| zfrom    |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The z coordinate of the position to look from. |
| xto      |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The x coordinate of the position to look to.   |
| yto      |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The y coordinate of the position to look to.   |
| zto      |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The z coordinate of the position to look to.   |
| xup      |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The x coordinate of the "up" vector.           |
| yup      |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The y coordinate of the "up" vector.           |
| zup      |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The z coordinate of the "up" vector.           |

#### Returns:

``` gml
 Matrix Array
```

#### Example:

``` gml
viewmat = matrix_build_lookat(640, 240, -10, 640, 240, 0, 0, 1, 0);
projmat = matrix_build_projection_ortho(640, 480, 1.0, 32000.0);
camera_set_view_mat(view_camera[0], viewmat);
camera_set_proj_mat(view_camera[0], projmat);
```

The above code creates a new look-at matrix and orthographic matrix,
stores their IDs in local variables and then uses them to set the view
and projection matrices for the camera assigned to view port\[0\].

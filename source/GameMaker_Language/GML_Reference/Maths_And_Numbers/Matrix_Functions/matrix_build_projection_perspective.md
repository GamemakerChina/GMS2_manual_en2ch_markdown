# matrix_build_projection_perspective

This function builds a perspective projection matrix based on the
dimensions of the near clipping plane, using the specified parameters
listed below. Note that the field of view of the camera will vary
depending on the width , height and znear values specified, as the
projection width and height are placed at the Z position specified in
the znear argument. For example, given a constant size of 640x480, the
field of view will be wider if znear is closer to the camera, but it
will be narrower if znear is far away from the camera. This behaviour is
demonstrated in the following visual:  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/GML/Reference/Maths/matrix_perspective_znear_dimensions.png)  
Due to this, it is recommended to use a znear value that is identical to
the width of the projection, resulting in the field of view being
consistent with an equivalent orthographic projection.

#### Syntax:

``` gml
matrix_build_projection_perspective(width, height, znear, zfar);
```

|          |                                                                         |                                                      |
|----------|-------------------------------------------------------------------------|------------------------------------------------------|
| Argument | Type                                                                    | Description                                          |
| w        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The width of the projection at the near Z position.  |
| h        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The height of the projection at the near Z position. |
| znear    |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The near clipping plane.                             |
| zfar     |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The far clipping plane.                              |

#### Returns:

``` gml
 Matrix Array
```

#### Example:

``` gml
var projmat = matrix_build_projection_perspective(640, 480, 640.0, 32000.0);
camera_set_proj_mat(view_camera[0], projmat);
```

The above code creates a perspective projection and then uses the matrix
returned to set the camera assigned to view port\[0\].

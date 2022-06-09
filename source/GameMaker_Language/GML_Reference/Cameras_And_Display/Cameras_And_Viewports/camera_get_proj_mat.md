# camera_get_proj_mat

This function can be used to retrieve the projection matrix. The
function returns the matrix array which can then be used in other
[matrix
functions](../../Maths_And_Numbers/Matrix_Functions/Matrix_Functions)
or to set the projection matrix of another camera (using [
camera_set_proj_mat() ](camera_set_proj_mat) ).

#### Syntax:

``` gml
camera_get_proj_mat(camera_id)
```

|           |                                                                                                                            |                                                                 |
|-----------|----------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| Argument  | Type                                                                                                                       | Description                                                     |
| camera_id |  [Camera ID](../../../../../GameMaker_Language/GML_Reference/Cameras_And_Display/Cameras_And_Viewports/camera_create)  | The unique camera ID value returned when you created the camera |

#### Returns:

``` gml
 Matrix Array
```

#### Example:

``` gml
mat = camera_get_proj_mat(camera_view[0]);
```

The above code gets the projection matrix for the camera assigned to
view port\[0\].

# camera_get_view_mat

This function can be used to retrieve the view matrix. The function
returns the matrix array which can then be used in other [matrix
functions](../../Maths_And_Numbers/Matrix_Functions/Matrix_Functions)
or to set the view matrix of another camera (using [
camera_set_view_mat() ](camera_set_view_mat) ). Note that this
function is generally for use with cameras created using [
camera_create() ](camera_create) , but it can also be used on those
created in the room editor (or with [ camera_create_view()
](camera_create_view) ) - in which case the returned matrix will
only be valid after the given camera is used in a view port for the
first time.

#### Syntax:

``` gml
camera_get_view_mat(camera_id)
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
mat = camera_get_view_mat(camera_view[0]);
```

The above code gets the view matrix for the camera assigned to view
port\[0\].

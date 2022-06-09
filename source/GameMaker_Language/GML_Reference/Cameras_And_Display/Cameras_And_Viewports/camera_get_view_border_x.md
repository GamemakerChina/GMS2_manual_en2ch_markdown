# camera_get_view_border_x

This function can be used to retrieve the border value for
object/instance following of the given camera along the x axis
(horizontal border). The return value will be in pixels.

#### Syntax:

``` gml
camera_get_view_border_x(camera_id)
```

|           |                                                                                                                            |                                                                 |
|-----------|----------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| Argument  | Type                                                                                                                       | Description                                                     |
| camera_id |  [Camera ID](../../../../../GameMaker_Language/GML_Reference/Cameras_And_Display/Cameras_And_Viewports/camera_create)  | The unique camera ID value returned when you created the camera |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
var xb = camera_get_view_border_x(view_camera[0]);
var yb = camera_get_view_border_y(view_camera[0]);
if xb != 200 || yb != 200
{
    camera_set_view_border(view_camera[0], 200, 200);
}
```

The above code retrieves the xborder and yborder values of the camera
assigned to view port\[0\] and then checks this to see if it matches the
given value. If it does not then the view camera is set to the given
value.

# camera_get_view_speed_y

This function can be used to retrieve the movement speed of the given
camera along the y axis (vertical movement). The return value will be in
pixels per game frame.

#### Syntax:

``` gml
camera_get_view_speed_y(camera_id)
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
var xs = camera_get_view_speed_x(view_camera[0]);
var ys = camera_get_view_speed_y(view_camera[0]);
if xs != 5 || ys != 5
{
    camera_set_view_speed(view_camera[0], 5, 5);
}
```

The above code retrieves the xspeed and yspeed of the camera assigned to
view port\[0\] and then checks this to see if it matches the given
value. If it does not then the view camera is set to that speed.

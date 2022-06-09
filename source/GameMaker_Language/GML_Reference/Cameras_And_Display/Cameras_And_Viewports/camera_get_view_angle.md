# camera_get_view_angle

This function can be used to retrieve the angle of the given camera. The
return value will be between 0 and 360. Note that this function is
*only* valid for cameras created using [ camera_create_view()
](camera_create_view) or for those added in the room editor.

#### Syntax:

``` gml
camera_get_view_angle(camera_id)
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
var ang = camera_get_view_angle(view_camera[0]);
if ang != 0
{
    camera_set_view_angle(view_camera[0], 0);
}
```

The above code retrieves the angle of the camera assigned to view
port\[0\] and then checks this to see if it matches the given value. If
it does not then the view camera is set to that angle.

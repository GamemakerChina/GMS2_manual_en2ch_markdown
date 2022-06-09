# camera_get_view_x

This function can be used to retrieve the x position of the view for a
given camera. Note that this function is *only* valid for cameras
created using [ camera_create_view() ](camera_create_view) or for
those added in the room editor.

#### Syntax:

``` gml
camera_get_view_x(camera_id)
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
var vx = camera_get_view_x(view_camera[0]); var vy = camera_get_view_y(view_camera[0]); draw_text(vx + 5, vy + 5, "SCORE" + string(score));
```

The above code retrieves the position of the camera assigned to view
port\[0\] and then draws text relative to that position.

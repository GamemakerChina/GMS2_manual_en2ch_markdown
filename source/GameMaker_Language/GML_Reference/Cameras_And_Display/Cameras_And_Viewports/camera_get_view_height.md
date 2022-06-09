# camera_get_view_height

This function can be used to retrieve the height (in pixels) of the
given camera. Note that this function is *only* valid for cameras
created using [ camera_create_view() ](camera_create_view) or for
those added in the room editor.

#### Syntax:

``` gml
camera_get_view_height(camera_id)
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
var vw = camera_get_view_width(view_camera[0]) / 2; var vh = camera_get_view_height(view_camera[0]) / 2; camera_set_view_pos(view_camera[0], x - vw, y - vh);
```

The above code retrieves the width and height of the camera assigned to
view port\[0\] and then sets its position relative to the center.

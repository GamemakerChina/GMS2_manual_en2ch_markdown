# camera_set_view_border

You can use this function to set the follow border of the view camera
within the room. You give the unique camera ID value (as returned by the
different camera_create functions) and then give the x border size and
the y border size (horizontal and vertical). These values will only be
used when the view camera has been assigned an instance target to follow
(either in the Room Editor or using the function [
camera_set_view_target() ](camera_set_view_target) ) and relate to
how far from the border of the view the instance needs to be before the
view will update its position to follow.

#### Syntax:

``` gml
camera_set_view_border(camera_id, x_border, y_border)
```

|           |                                                                                                                            |                                                                      |
|-----------|----------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| Argument  | Type                                                                                                                       | Description                                                          |
| camera_id |  [Camera ID](../../../../../GameMaker_Language/GML_Reference/Cameras_And_Display/Cameras_And_Viewports/camera_create)  | The unique camera ID value returned when you created the camera.     |
| x_border  |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                     | The border (in pixels) for the view camera along the horizontal axis |
| y_border  |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                     | The border (in pixels) for the view camera along the vertical axis   |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
camera_set_view_border(view_camera[0], 64, 64);
```

The above code will set the view camera border for the camera assigned
to view port\[0\].

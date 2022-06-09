# camera_set_view_angle

You can use this function to update the angle of the view camera within
the room. You give the unique camera ID value (as returned by the
different [ camera_create() ](camera_create) functions) and then
give the angle that you wish to set the camera view to. The default
value is 0° with positive values rotating the camera
**counter-clockwise** , ie: setting the value to 90 will rotate the
camera 90° to the left.

#### Syntax:

``` gml
camera_set_view_angle(camera_id, angle)
```

|           |                                                                                                                            |                                                                 |
|-----------|----------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| Argument  | Type                                                                                                                       | Description                                                     |
| camera_id |  [Camera ID](../../../../../GameMaker_Language/GML_Reference/Cameras_And_Display/Cameras_And_Viewports/camera_create)  | The unique camera ID value returned when you created the camera |
| angle     |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                     | The new angle to set the camera view to                         |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
camera_set_view_angle(view_camera[0], point_direction(x, y, mouse_x, mouse_y));
```

The above code will set the view camera angle for the camera assigned to
view port\[0\].

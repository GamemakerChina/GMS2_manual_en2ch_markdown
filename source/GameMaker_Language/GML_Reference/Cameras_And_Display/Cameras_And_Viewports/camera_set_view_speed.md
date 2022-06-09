# camera_set_view_speed

You can use this function to update the speed of the view camera within
the room. You give the unique camera ID value (as returned by the
different [ camera_create() ](camera_create) functions) and then
give the x and y (horizontal and vertical) speed that it should move
when set to follow a given instance. The speed is calculated as pixels
per step and can be set to "-1" to make the camera move instantly, but
if the camera is not set to follow any instance then the values set here
will have no visible effect.

#### Syntax:

``` gml
camera_set_view_speed(camera_id, xspeed, yspeed)
```

|           |                                                                                                                            |                                                                                                  |
|-----------|----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| Argument  | Type                                                                                                                       | Description                                                                                      |
| camera_id |  [Camera ID](../../../../../GameMaker_Language/GML_Reference/Cameras_And_Display/Cameras_And_Viewports/camera_create)  | The unique camera ID value returned when you created the camera.                                 |
| xspeed    |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                     | The speed (number of pixels per game frame) that the view should move on the horizontal (x) axis |
| yspeed    |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                     | The speed (number of pixels per game frame) that the view should move on the vertical (y) axis   |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
camera_set_view_speed(view_camera[0], 5, 5);
```

The above code will set the view camera speed for the camera assigned to
view port\[0\].

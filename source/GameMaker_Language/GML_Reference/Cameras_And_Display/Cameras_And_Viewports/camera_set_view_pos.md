# camera_set_view_pos

You can use this function to update the position of the camera view
within the room. You give the unique camera ID value (as returned by the
different [camera_create()](camera_create) functions) and then give
the x and y positions to set the camera to.

#### Syntax:

``` gml
camera_set_view_pos(camera_id, x, y)
```

|           |                                                                                                                            |                                                                  |
|-----------|----------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| Argument  | Type                                                                                                                       | Description                                                      |
| camera_id |  [Camera ID](../../../../../GameMaker_Language/GML_Reference/Cameras_And_Display/Cameras_And_Viewports/camera_create)  | The unique camera ID value returned when you created the camera. |
| x         |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                     | The x position to place the view at (in the room)                |
| y         |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                     | The y position to place the view at (in the room)                |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
camera_set_view_pos(view_camera[0], x - (view_wport[0] / 2), y - (view_hport[0] / 2));
```

The above code will set the view camera position for the camera assigned
to view port\[0\].

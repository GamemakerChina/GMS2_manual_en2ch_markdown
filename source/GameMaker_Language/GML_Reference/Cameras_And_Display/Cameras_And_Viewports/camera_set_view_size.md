# camera_set_view_size

You can use this function to update the size of the view camera within
the room. You give the unique camera ID value (as returned by the
different [ camera_create() ](camera_create) functions) and then
give the width and height (in pixels) to set the camera to.

#### Syntax:

``` gml
camera_set_view_size(camera_id, width, height)
```

|           |                                                                                                                            |                                                                  |
|-----------|----------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| Argument  | Type                                                                                                                       | Description                                                      |
| camera_id |  [Camera ID](../../../../../GameMaker_Language/GML_Reference/Cameras_And_Display/Cameras_And_Viewports/camera_create)  | The unique camera ID value returned when you created the camera. |
| width     |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                     | The width of the camera view in pixels                           |
| height    |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                     | The height of the camera view in pixels                          |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
camera_set_view_size(view_camera[0], view_wport[0], view_hport[0]);
```

The above code will set the view camera size for the camera assigned to
view port\[0\].

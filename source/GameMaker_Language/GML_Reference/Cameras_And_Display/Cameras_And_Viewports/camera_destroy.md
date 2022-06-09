# camera_destroy

With this function you can destroy any camera. When calling the function
you supply the unique camera ID value, which you get from the
camera_create\_\* functions or from the [ view_camera ](view_camera)
array if using the Room Editor to set up the view port and view. You
should *never* destroy a camera that is currently assigned to a visible
view, unless you are assigning a new camera to that view in the same
step, and you should *always* destroy any cameras that you have created
through code when no longer required by your game to prevent memory
leaks, and you can also destroy the default cameras if you have any
assigned in the Room Editor, but you should assign a new camera to the
view port (or disable it) otherwise you will get odd results.

#### Syntax:

``` gml
camera_destroy(camera_id)
```

|           |                                                                                                                            |                                                                  |
|-----------|----------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| Argument  | Type                                                                                                                       | Description                                                      |
| camera_id |  [Camera ID](../../../../../GameMaker_Language/GML_Reference/Cameras_And_Display/Cameras_And_Viewports/camera_create)  | The unique camera ID value returned when you created the camera. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
camera_destroy(view_camera[0]);
view_camera[0] = camera_create_view(0, 0, 640, 480, 0, obj_Player, 5, 5, -1, -1);
```

The above code destroys the camera currently assigned to view port \[0\]
then creates a new camera and assigns its ID to that port.

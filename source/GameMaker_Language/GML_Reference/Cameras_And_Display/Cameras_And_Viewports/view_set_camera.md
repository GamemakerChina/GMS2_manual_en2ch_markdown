# view_set_camera

This function will set a camera to a specific view port. You give the
view port to set (from 0 to 7), and supply the unique camera ID value
(as returned by the [ camera_create() ](camera_create) functions or
when you use [ view_get_camera() ](view_get_camera) ). If you give a
value of -1 as the camera ID then you are removing a camera from the
view port and note that if that view port is enabled and visible you may
get some unpredictable results.

#### Syntax:

``` gml
view_set_camera(view_port, camera_id)
```

|           |                                                                                                                            |                                                                 |
|-----------|----------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| Argument  | Type                                                                                                                       | Description                                                     |
| view_port |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                     | The view port to target (0 - 7)                                 |
| camera_id |  [Camera ID](../../../../../GameMaker_Language/GML_Reference/Cameras_And_Display/Cameras_And_Viewports/camera_create)  | The unique camera ID value returned when you created the camera |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
var cam = camera_create_view(0, 0, 640, 480, 0, obj_Player, 5, 5, -1, -1); view_set_camera(0, cam);
```

The above code will create a new camera and then assign it view
port\[0\].

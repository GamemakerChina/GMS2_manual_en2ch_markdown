# view_get_camera

This function can be used to retrieve the unique camera ID value for the
camera assigned to the given view port (from 0 - 7). If no camera is
assigned, the function will return -1.

#### Syntax:

``` gml
view_get_camera(view_port)
```

|           |                                                                         |                                 |
|-----------|-------------------------------------------------------------------------|---------------------------------|
| Argument  | Type                                                                    | Description                     |
| view_port |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The view port to target (0 - 7) |

#### Returns:

``` gml
 Camera ID
```

#### Example:

``` gml
var cam = view_get_camera(0);
var cw = camera_get_view_width(cam);
var ch = camera_get_view_height(cam);
camera_set_view_pos(cam, mouse_x - (cw / 2), mouse_y - (ch / 2));
```

The above code will retrieve the camera ID for the camera assigned to
view port\[0\] and then change its position.

# camera_create_view

This function will create a new camera and then set its view into the
room, before return the unique ID value to identify the camera in future
function calls. The camera will be created using the values that you set
in this function for position, size and other details which correlate to
the values you set in the Room Editor (see
[here](../../../../The_Asset_Editors/Rooms) ). Note that this
function can take a *variable number of arguments* with only the x/y
position and width/height arguments being obligatory. Any arguments not
supplied will use their default arguments. Note that cameras are like
all dynamic resources and will occupy memory when created. This means
that you need to take care not to create cameras unnecessarily and to
destroy those that you don't need by calling the function [
camera_destroy() ](camera_destroy) . This also means that cameras
will persist from room to room if assigned to a global variable (they
will persist when assigned to instance or local variables too, but you
can't access them after changing room, hence the memory leak), so that
you can - for example - create a new camera, assign it to a global
variable, and then at the start of each room use the camera_set\_\*
functions to set the properties before assigning it to a view port.

#### Syntax:

``` gml
camera_create_view(room_x, room_y, width, height, [angle, object, x_speed, y_speed, x_border, y_border])
```

|          |                                                                                                                                                                                         |                                                                                                                                                                                                      |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Argument | Type                                                                                                                                                                                    | Description                                                                                                                                                                                          |
| room_x   |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                                                                  | The x position (within the room) of the left side of the area the camera view captures.                                                                                                              |
| room_y   |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                                                                  | The y position (within the room) of the top of the area the camera view captures.                                                                                                                    |
| width    |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                                                                  | The width of the area the view captures.                                                                                                                                                             |
| height   |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                                                                  | The height of the area the view captures.                                                                                                                                                            |
| angle    |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                                                                  |  OPTIONAL The angle to set the for the camera view(from 0° - 360°, default is 0).                                                                                                                    |
| object   |  [Object Asset](../../../../../The_Asset_Editors/Objects) or [Instance ID](../../../../../GameMaker_Language/GML_Reference/Asset_Management/Instances/Instance_Variables/id)    |  OPTIONAL The object ID (or instance ID) for the camera view to follow (default is -1, no object).                                                                                                   |
| x_speed  |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                                                                  |  OPTIONAL The maximum horizontal speed the view can move at (set to -1 for "instant" following, default is -1).                                                                                      |
| y_speed  |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                                                                  |  OPTIONAL The maximum vertical speed the view can move at (set to -1 for "instant" following, default is -1).                                                                                        |
| x_border |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                                                                  |  OPTIONAL The minimum horizontal space between the edge of the view area and the instance it is set to follow (before the view begins moving and if it is set to follow an instance, default is 0).  |
| y_border |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                                                                  |  OPTIONAL The minimum vertical space between the edge of the view area and the instance it is set to follow (before the view begins moving and if it is set to follow an instance, default is 0).    |

#### Returns:

``` gml
 Camera ID
```

#### Example:

``` gml
camera_destroy(view_camera[0]);
view_camera[0] = camera_create_view(0, 0, 640, 480, 0, obj_Player, 5, 5, -1, -1);
```

The above code removes the current camera assigned to viewport\[0\] and
then creates a new camera, defines its view properties and then assigns
that to viewport\[0\].

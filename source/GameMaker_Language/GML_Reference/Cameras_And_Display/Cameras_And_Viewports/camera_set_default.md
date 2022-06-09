# camera_set_default

This function can be used to set the default camera to use a custom
camera that you have previously created using one of the [
camera_create() ](camera_create) functions. When you create a room
with *no* active view ports or view cameras, GameMaker still uses a
camera to show the action in the game. This camera is called the
**default** camera and can be set and manipulated (and even destroyed)
just like any other camera.

#### Syntax:

``` gml
camera_set_default(camera_id)
```

|           |                                                                                                                            |                                                                 |
|-----------|----------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| Argument  | Type                                                                                                                       | Description                                                     |
| camera_id |  [Camera ID](../../../../../GameMaker_Language/GML_Reference/Cameras_And_Display/Cameras_And_Viewports/camera_create)  | The unique camera ID value returned when you created the camera |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
var new_cam = camera_create_view(0, 0, 640, 480, 0, obj_Player, 5, 5, -1, -1); camera_set_default(new_cam);
```

The above code creates a new camera and then assigns it as the default
camera to use.

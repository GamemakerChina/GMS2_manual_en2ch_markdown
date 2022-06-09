# camera_get_default

This function can be used to retrieve the unique camera ID value of the
default camera (the camera that GameMaker uses when no camera views or
ports are active in a game room).

#### Syntax:

``` gml
camera_get_default()
```

#### Returns:

``` gml
 Camera ID
```

#### Example:

``` gml
var def = camera_get_default();
view_camera[0] = def;
```

The above code gets the camera ID for the default camera and sets the
view camera for port\[0\] to use it.

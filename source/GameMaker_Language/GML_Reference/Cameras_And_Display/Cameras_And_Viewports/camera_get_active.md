# camera_get_active

This function can be used to retrieve the unique camera ID value of the
currently active camera.

#### Syntax:

``` gml
camera_get_active()
```

#### Returns:

``` gml
 Camera ID
```

#### Example:

``` gml
var active = camera_get_active();
if active != view_camera[0]
{
    view_camera[0] = active;
}
```

The above code gets the camera ID for the active camera and sets the
view camera for port\[0\] to use it.

# instance_activate_all

With this function you can tell GameMaker to activate all instances that
have been previously deactivated in a room. Note that activation is not
instantaneous, and an instance that has been activated in this way will
not be considered to be active until the end of the event in which the
function was called.

#### Syntax:

``` gml
instance_activate_all();
```

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
instance_activate_all(); var _vx = camera_get_view_x(view_camera[0]); var _vy = camera_get_view_y(view_camera[0]); var _vw = camera_get_view_width(view_camera[0]); var _vh = camera_get_view_height(view_camera[0]); instance_deactivate_region(_vx
- 64, _vy - 64, _vw + 128, _vh + 128, false, false);
```

The above code activates all instances within the room and then
deactivates those that are 64px outside of the limits of the current
camera view.

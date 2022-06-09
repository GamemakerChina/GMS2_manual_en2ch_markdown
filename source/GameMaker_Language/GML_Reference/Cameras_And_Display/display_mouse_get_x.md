# display_mouse_get_x

This function will return the mouse x position within the *screen* . It
should be noted that this function only works properly when used on the
Windows and macOS targets. It can be used for HTML5 too, but will only
return a value *relative* to the 0,0 of the canvas itself, and will not
return any value while the mouse is outside of the canvas. For other
devices it will return 0, and you should use the [ device_mouse_raw_x()
](../Game_Input/Device_Input/device_mouse_raw_x) and [
device_mouse_raw_y()
](../Game_Input/Device_Input/device_mouse_raw_y) functions instead.

#### Syntax:

``` gml
display_mouse_get_x();
```

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
my_x = display_mouse_get_x();
```

This would set my_x to the x coordinate of the mouse relative to the
display.

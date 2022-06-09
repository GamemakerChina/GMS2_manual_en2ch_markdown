# application_surface_is_enabled

This function will return true if the application surface is being used
for drawing, or false if the screen buffer is being used.

#### Syntax:

``` gml
application_surface_is_enabled();
```

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
if keyboard_check_pressed(vk_space)
{
    if application_surface_is_enabled()
    {
        application_surface_enable(false);
    }
    else
    {
        application_surface_enable(true);
    }
}
```

The above code check for a key press and the toggle the application
surface on or off depending on its state (like in an options menu).

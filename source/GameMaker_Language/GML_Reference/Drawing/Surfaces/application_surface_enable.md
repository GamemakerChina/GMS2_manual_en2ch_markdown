# application_surface_enable

With this function you can enable or disable the application surface. By
default the application surface is enabled and all drawing for the Draw
events will be done to that and the surface drawn to the screen. However
on some older devices and specific chipsets this may result in poorer
performance. In those cases you can switch off drawing to the
application surface and all Draw event drawing will then be done
directly to the screen buffer. You can use this function to enable or
disable the application surface at any time in your game, but you should
note that it requires at least one frame (step) for the changes to take
effect. Switching it off ***will switch off all aspect ratio
correction*** , as set in the *Game Options* for the target platform.
This means that you should have some method in place that scales the
game to the required device, window or screen dimensions. If you switch
it back on again, then the *Game Options* will take effect again the
next step. It is recommended that you use this function carefully as it
will impact on how everything is drawn to the screen. In general you
would want to have it as an option in a menu of your game, or call it
only once at the start of your game and write your code around whether
you have it enabled or disabled.

#### Syntax:

``` gml
application_surface_enable(enable);
```

|          |                                                                            |                                                                          |
|----------|----------------------------------------------------------------------------|--------------------------------------------------------------------------|
| Argument | Type                                                                       | Description                                                              |
| enable   |  [Boolean](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | Set to enable ( true ) or disable ( false ) the application surface.     |

#### Returns:

``` gml
N/A
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

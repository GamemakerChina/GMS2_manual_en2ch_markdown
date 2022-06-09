# window_center

With this function you can center the game window in the display when
the target module is Windows, Ubuntu (Linux) or macOS, or you can center
it in the browser if the target module is HTML5. This function has no
effect on any other device. **NOTE** If you have resized the game window
in the current step (for example, by switching from full screen to
windowed or using [window_set_size()](window_set_size) ), and wish
to center the new window, this function should be called at least one
step later (for example, by using an
[alarm](../../Asset_Management/Instances/Instance_Variables/alarm)
) otherwise it will not work correctly.

#### Syntax:

``` gml
window_center();
```

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if !window_get_fullscreen()
{
    window_center();
}
```

The above code will center the game window within the display if it is
not in full screen mode.

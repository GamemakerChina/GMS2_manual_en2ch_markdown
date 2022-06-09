# window_get_fullscreen

This function returns whether the game window is in fullscreen mode (
true ) or not ( false ).

#### Syntax:

``` gml
window_get_fullscreen();
```

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
if window_get_fullscreen()
{
    draw_text(32, 32, "Fullscreen is ON");
}
else
{
    draw_text(32, 32, "Fullscreen is OFF");
}
```

The above code will check to see if the window is in full screen mode or
not and draw a text message depending on the returned value.

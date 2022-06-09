# window_views_mouse_get_x

This function returns the x-coordinate of the mouse with respect to all
the active views and returns the same value [ mouse_x
](../../Game_Input/Mouse_Input/mouse_x) . **NOTE** : For regular
mouse functions see the section on [Mouse
Input](../../Game_Input/Mouse_Input/Mouse_Input) .

#### Syntax:

``` gml
window_views_mouse_get_x();
```

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
myx = window_views_mouse_get_x();
```

This would set myx to the x coordinate of the mouse in the window
relative to all active views.

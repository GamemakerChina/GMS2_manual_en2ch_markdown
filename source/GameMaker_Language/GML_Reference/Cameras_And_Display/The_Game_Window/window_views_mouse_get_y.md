# window_views_mouse_get_y

This function returns the y-coordinate of the mouse with respect to all
the active views and returns the same value [ mouse_y
](../../Game_Input/Mouse_Input/mouse_y) . **NOTE** : For regular
mouse functions see the section on [Mouse
Input](../../Game_Input/Mouse_Input/Mouse_Input) .

#### Syntax:

``` gml
window_views_mouse_get_y();
```

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
myy = window_views_mouse_get_y();
```

This would set myy to the y coordinate of the mouse in the window
relative to all active views.

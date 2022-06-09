# window_mouse_get_x

With this function you can get the x position of the mouse cursor (in
pixels) within the browser if it is an HTML5 game or within the display
if it is a Windows, Ubuntu (Linux) or macOS game. **NOTE** : For regular
mouse functions see the section on [Mouse
Input](../../Game_Input/Mouse_Input/Mouse_Input)

#### Syntax:

``` gml
window_mouse_get_x();
```

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
wx = window_mouse_get_x();
```

The above code stores the current x axis window position of the mouse in
the variable "wx".

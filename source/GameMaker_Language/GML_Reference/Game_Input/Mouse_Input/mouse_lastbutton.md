# mouse_lastbutton

This variable returns the last mouse button that was pressed and can
return any of the special [mouse constants](Mouse_Input) except
mb_any (you may also set this variable to one of the constants).

#### Syntax:

``` gml
mouse_lastbutton;
```

#### Returns:

``` gml
 Mouse Button Constant

(except mb_any)
```

#### Example:

``` gml
if mouse_lastbutton = mb_left
{
    x -= 1;
}
```

This moves the current instance left if the last button pressed was the
left mouse button.

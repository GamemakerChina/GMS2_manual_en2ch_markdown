# mouse_button

This **read only** variable returns the mouse button that is currently
being pressed (currently, as in, this step) and can return any of the
special [mouse constants](Mouse_Input) except mb_any .

#### Syntax:

``` gml
mouse_button;
```

#### Returns:

``` gml
 Mouse Button Constant

(except mb_any)
```

#### **Example:**

``` gml
if mouse_button = mb_left
{
    x -= 1;
}
```

This moves the current instance left if the left mouse button is down.

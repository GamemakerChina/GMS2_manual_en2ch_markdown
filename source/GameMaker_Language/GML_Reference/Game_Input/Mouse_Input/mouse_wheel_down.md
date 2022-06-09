# mouse_wheel_down

This function returns true if the mouse wheel is being rotated downwards
and false otherwise.

#### Syntax:

``` gml
mouse_wheel_down();
```

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
if mouse_wheel_down()
{
    y += 10;
}
```

This moves the current instance down the screen if the mouse wheel is
rotated upwards.

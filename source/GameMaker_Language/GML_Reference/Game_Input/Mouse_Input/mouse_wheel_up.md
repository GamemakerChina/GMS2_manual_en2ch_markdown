# mouse_wheel_up

This function returns true if the mouse wheel is being rotated upwards
and false otherwise.

#### Syntax:

``` gml
mouse_wheel_up();
```

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
if mouse_wheel_up()
{
    y -= 10;
}
```

This moves the current instance up the screen if the mouse wheel is
rotated upwards.

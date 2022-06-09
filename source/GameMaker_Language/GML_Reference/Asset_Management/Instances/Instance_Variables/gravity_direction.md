# gravity_direction

gravity_direction is one of the "built in" properties all instances have
and can be used to set the direction of movement when the instances [
gravity ](gravity) is greater than 0. Note that directions in
GameMaker are usually calculated as 0° being right, 90° being up, 180°
being left and 270° being down.

#### Syntax:

``` gml
gravity_direction;
```

#### Returns:

``` gml
 Real

(single precision floating point value)
```

#### Example:

``` gml
if place_meeting(x, y, obj_switch)
{
    gravity_direction += 180;
}
```

The above code will change the gravity_direction if the player object
meets an instance of "obj_switch".

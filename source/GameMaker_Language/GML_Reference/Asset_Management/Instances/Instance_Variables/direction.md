# direction

All instances in GameMaker have certain "built in" properties that you
can use and set to govern how they look and behave. Direction is one of
those properties and can be used to set the direction of movement of the
instance when the instance has a [ speed ](speed) other than 0. Note
that directions in GameMaker are usually calculated as 0° being right,
90° being up, 180° being left and 270° being down, and that the [
gravity ](gravity) and [ gravity_direction ](gravity_direction)
variables can modify the direction value when they are used in your
games.

#### Syntax:

``` gml
direction;
```

#### Returns:

``` gml
 Real

(single precision floating point value)
```

#### Example:

``` gml
if keyboard_check(vk_left) direction += 5; if keyboard_check(vk_right) direction -= 5;
```

The above code will change the direction of movement of the instance
based on which key (left or right) is pressed.

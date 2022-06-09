# speed

All instances in GameMaker have certain "built in" properties that you
can use and set to govern how they look and behave. speed is one of
those properties and defines how many pixels the instance will move
every step. Unlike [ hspeed ](hspeed) and [ vspeed ](vspeed) ,
speed has no direction associated with it as this is governed by the [
direction ](direction) value of the instance, but it can have a
negative value, in which case the instance will travel in the opposite
direction to that set by the direction function (ie: direction  - 180°).
Note that setting the speed and/or the direction , will also modify the
values of the hspeed and vspeed variables, and that [ gravity
](gravity) , [ gravity_direction ](gravity_direction) and [
friction ](friction) can all modify the value of this variable when
they are used in your games.

#### Syntax:

``` gml
speed;
```

#### Returns:

``` gml
 Real

(single precision floating point value)
```

#### Example:

``` gml
if keyboard_check(vk_up) speed = 2; if keyboard_check(vk_left) direction += 5; if keyboard_check(vk_right) direction -= 5;
```

The above code will use the arrow keys to set the speed and direction of
the instance.

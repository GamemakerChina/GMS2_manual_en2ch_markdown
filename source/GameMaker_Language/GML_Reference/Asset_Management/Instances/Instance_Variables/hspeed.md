# hspeed

hspeed is one of the "built in" properties that all instances have and
defines the horizontal movement speed (along the x-axis) of the instance
in pixels per step. So, an hspeed of 3 means 3 pixels of movement to the
right (+x) every step, and an hspeed of -3 would mean 3 pixels of
movement to the left (-x) every step. Note that if you set the
[speed](speed) and/or [direction](direction) variables then the
hspeed value will be updated automatically to reflect these changes, and
likewise, changing the hspeed value will also affect the speed and
direction values. Also note that [ gravity ](gravity) , [
gravity_direction ](gravity_direction) and [ friction
](friction) can all modify the value of this variable when they are
used in your games.

#### Syntax:

``` gml
hspeed;
```

#### Returns:

``` gml
 Real

(single precision floating point value)
```

#### Example:

``` gml
if keyboard_check(vk_left) hspeed = -5; if keyboard_check(vk_right) hspeed = 5;
```

The above code will change the horizontal speed depending on which keys
are pressed.

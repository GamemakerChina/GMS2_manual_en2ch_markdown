# vspeed

vspeed is one of the "built in" properties that all instances have and
defines the vertical movement speed (along the y-axis) of the instance
in pixels per step. So, a vspeed of 3 means 3 pixels of movement to the
bottom (+y) every step, and a vspeed of -3 would mean 3 pixels of
movement to the top (-y) every step. Note that if you set the
[speed](speed) and/or [direction](direction) variables then the
vspeed value will be updated automatically to reflect these changes, and
likewise, changing the vspeed value will also affect the speed and
direction values. Also note that [ gravity ](gravity) , [
gravity_direction ](gravity_direction) and [ friction
](friction) can all modify the value of this variable when they are
used in your games.

#### Syntax:

``` gml
vspeed;
```

#### Returns:

``` gml
 Real

(single precision floating point value)
```

#### Example:

``` gml
if keyboard_check(vk_up) vspeed = -5; if keyboard_check(vk_down) vspeed = 5;
```

The above code will change the vertical speed depending on which keys
are pressed.

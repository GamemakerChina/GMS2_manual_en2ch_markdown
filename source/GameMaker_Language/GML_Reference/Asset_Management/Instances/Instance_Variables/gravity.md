# gravity

gravity is one of the "built in" variables all instances have and, when
set, will apply a constant force in the [ gravity_direction
](gravity_direction) of the instance, influencing both the instance
[speed](speed) and [direction](direction) . Note that gravity is
a cumulative force and will accelerate the object if you choose not to
cap the final speed, and it's usual that you'd set this variable to
small decimal values like 0.01. If you set the gravity to 0, then no
gravity will be applied to the instance (this is the default value).

#### Syntax:

``` gml
gravity;
```

#### Returns:

``` gml
 Real

(single precision floating point value)
```

#### Example:

``` gml
if !place_meeting(x, y + 1, obj_Ground)
{
    gravity = 0.01;
}
else
{
    gravity = 0;
}
```

The above code will only apply gravity if the instance does not find any
instances of "obj_Ground" beneath it.

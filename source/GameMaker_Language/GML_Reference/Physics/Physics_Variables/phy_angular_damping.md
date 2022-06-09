# phy_angular_damping

This variable can be used to set the angular damping of the instance, or
it can be used to get the current angular damping. The damping is the
amount of "resistance" to angular rotation that the physics enabled
instance has, with a lower value permitting the instance to rotate
faster after a collision (for example) and a higher value making it
require a more forceful push and rotate slower

#### Syntax:

``` gml
phy_angular_damping;
```

#### Returns:

``` gml
 Real

(single precision floating point value, or undefined if the instance is not physics enabled)
```

#### Example:

``` gml
if place_meeting(phy_position_x, phy_position_y, obj_Water)
{
    phy_angular_damping = 10;
}
else
{
    phy_angular_damping = 3;
}
```

The above code will check for a collision between the calling instance
and instances of "obj_Water" and change the angular damping accordingly.

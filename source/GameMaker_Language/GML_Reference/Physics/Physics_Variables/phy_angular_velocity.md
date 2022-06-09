# phy_angular_velocity

This variable can be used to set the angular velocity of the instance,
or it can be used to get the current angular velocity, in degrees per
second and the value used can be either positive (for clockwise
rotation) or negative (for anticlockwise rotation). If you set this on
an instance that was previously static (ie: it has a density of 0) it
will become a kinematic object and begin rotating

#### Syntax:

``` gml
phy_angular_velocity;
```

#### Returns:

``` gml
 Real

(single precision floating point value, or undefined if the instance is not physics enabled)
```

#### Example:

``` gml
if abs(phy_angular_velocity) &amp;gt; 0
{
    phy_angular_velocity -= sign(phy_angular_velocity) * 0.01;
}
else
{
    phy_angular_velocity = 0;
}
```

The above code will check the angular velocity of the instance and if it
is not 0 it will then add (or subtract) a small amount every step until
the value is 0.

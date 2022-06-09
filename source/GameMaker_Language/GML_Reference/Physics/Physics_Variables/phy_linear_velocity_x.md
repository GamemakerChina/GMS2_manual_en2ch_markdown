# phy_linear_velocity_x

This variable can be used to get or change the x component of the
instance's linear velocity vector and is defined in pixels per second
(for pixels per step, see [ phy_speed_x ](phy_speed_x) ). Altering
this for a static instance (ie: an instance with 0 density) will turn it
into a kinematic instance

#### Syntax:

``` gml
phy_linear_velocity_x;
```

#### Returns:

``` gml
 Real

(single precision floating point value, or undefined if the instance is not physics enabled)
```

#### Example:

``` gml
if (phy_linear_velocity_x != 0)
{
    phy_linear_velocity_x = 0;
}
```

The above code will check the x component of the linear velocity vector
and if it is anything other than 0 it will set it to 0.

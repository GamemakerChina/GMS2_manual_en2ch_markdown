# phy_speed_y

This variable can be used to get or change the y component of the
instance's linear speed vector and is defined in pixels per step (for
pixels per second, see [ phy_linear_velocity_y
](phy_linear_velocity_y) ). Altering this for a static instance (ie:
an instance with 0 density) will turn it into a kinematic instance.

#### Syntax:

``` gml
phy_speed_y;
```

#### Returns:

``` gml
 Real

(single precision floating point value, or undefined if the instance is not physics enabled)
```

#### Example:

``` gml
if phy_speed_y != 0
{
    phy_speed_y = 0;
}
```

The above code will check the y component of the linear speed vector and
if it is anything other than 0 it will set it to 0.

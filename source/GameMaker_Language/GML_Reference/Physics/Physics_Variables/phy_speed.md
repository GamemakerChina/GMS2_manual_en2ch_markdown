# phy_speed

This **read-only** variable returns the current speed of the physics
enabled instance, defined in pixels per step. Should you need to change
this value, you must do so by changing the x and y vectors using the
variables [ phy_speed_x ](phy_speed_x) and
[phy_speed_y](phy_speed_y) .

#### Syntax:

``` gml
phy_speed;
```

#### Returns:

``` gml
 Real

(single precision floating point value, or undefined if the instance is not physics enabled)
```

#### Example:

``` gml
if phy_speed &amp;gt; 10
{
    phy_linear_damping += 0.01;
}
else
{
    phy_linear_damping = 2;
}
```

The above code checks the speed of the physics enabled instance and then
changes the linear damping based on the returned value.

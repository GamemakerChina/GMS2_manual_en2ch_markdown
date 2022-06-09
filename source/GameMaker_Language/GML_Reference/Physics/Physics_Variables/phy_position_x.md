# phy_position_x

This variable can be used to get (or to set) the x position of the
instance within the game room physics world. Please note that the
physics world may present errors when instances are moved by directly
setting this variable as it will interrupt the continuous simulation.
This variable is the physics equivalent of the instance variable
[x](../../Asset_Management/Instances/Instance_Variables/x) .

#### Syntax:

``` gml
phy_position_x;
```

#### Returns:

``` gml
 Real

(single precision floating point value, or undefined if the instance is not physics enabled)
```

#### Example:

``` gml
xx = phy_position_x; yy = phy_position_y;
```

The above code stores the instance x and y position in two variables.

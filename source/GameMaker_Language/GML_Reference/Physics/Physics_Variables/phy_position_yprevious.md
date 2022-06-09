# phy_position_yprevious

This variable can be used to get (or to set) the previous y position of
the instance within the game room physics world. This is the position of
the instance within the physics world in the previous step to the
current one

#### Syntax:

``` gml
phy_position_yprevious;
```

#### Returns:

``` gml
 Real

(single precision floating point value, or undefined if the instance is not physics enabled)
```

#### Example:

``` gml
xx = phy_position_xprevious; yy = phy_position_yprevious;
```

The above code stores the previous x and y position for the physics
enabled instance in two variables.

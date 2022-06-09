# phy_com_y

This **read-only** variable will return the y position of the instance's
center of mass. This is calculated automatically based on the density,
inertia and mass of the instance as defined by the appropriate functions

#### Syntax:

``` gml
phy_com_y;
```

#### Returns:

``` gml
 Real

(single precision floating point value, or undefined if the instance is not physics enabled)
```

#### Example:

``` gml
xx = phy_com_x; yy = phy_com_y;
```

The above code sets two variables to the x and y position of the
instances center of mass.

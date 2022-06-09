# phy_kinematic

This **read-only** variable will return true if the instance is classed
as being a kinematic object, or false if it is not. A kinematic instance
is one that has infinite mass (a density of 0) but can move. So, to make
an instance kinematic, you would first create a static instance and then
set one or more of the instance variables related to movement (ie: [
phy_speed_x ](phy_speed_x) , [ phy_speed_y ](phy_speed_y) , or [
phy_angular_velocity ](phy_angular_velocity) )

#### Syntax:

``` gml
phy_kinematic;
```

#### Returns:

``` gml
 Boolean

(or undefined if the instance is not physics enabled)
```

#### Example:

``` gml
if !phy_kinematic
{
    phy_speed_x = 5;
}
```

The above code checks to see if the instance is kinematic and if it is
not, it sets the horizontal speed to 5.

# phy_collision_x

This **read-only** array returns the x position of all points detected
in a collision between two physics enabled instances. **NOTE** : This
variable is only available in the collision event of a physics enabled
instance.

#### Syntax:

``` gml
phy_collision_x;
```

#### Returns:

``` gml
 Real

(single precision floating point value, or undefined if the instance is not physics enabled)
```

#### Example:

``` gml
for(var i = 0; i &amp;lt; phy_collision_points; i += 1;)
{
    part_particles_create(global.Sname, phy_collision_x[i], phy_collision_y[i], global.Spark, 5);
}
```

The above code creates particles at all the defined points of a
collision between two physics enabled instances.

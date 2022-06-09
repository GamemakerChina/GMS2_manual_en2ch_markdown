# phy_collision_points

This **read-only** variable returns the number of points of collision
detected between the two objects in the collision **NOTE** : This
variable is only available in the collision event of a physics enabled
instance.

#### Syntax:

``` gml
phy_collision_points;
```

#### Returns:

``` gml
 Real

(integer value, or undefined if the instance is not physics enabled)
```

#### Example:

``` gml
for(var i = 0; i &amp;lt; phy_collision_points; i += 1;)
{
    part_particles_create(global.Sname, phy_collision_x[i], phy_collision_x[1], global.Spark, 5);
}
```

The above code creates particles at all the defined points of a
collision between two physics enabled instances.

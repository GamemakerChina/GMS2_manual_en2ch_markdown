# phy_dynamic

A dynamic instance is one that is fully simulated within the physics
world and this **read-only** variable will return true if the instance
being checked is fully simulated or false if it is not

#### Syntax:

``` gml
phy_dynamic;
```

#### Returns:

``` gml
 Boolean

(or undefined if the instance is not physics enabled)
```

#### Example:

``` gml
if other.phy_dynamic
{
    with (other)
    {
        var dir;
        dir = point_direction(x, y, other.x, other.y);
        physics_apply_impulse(x, y, x + lengthdir_x(100, dir), y + lengthdir_y(100, dir));
    }
}
```

The above code creates a new instance and then defines it as being a
"bullet" in the physics world before giving it a massive impulse along
the y axis.

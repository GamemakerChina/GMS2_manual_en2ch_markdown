# phy_col_normal_y

This **read-only** variable returns the y component of the collision
normal corresponding to the [ phy_collision_y ](phy_collision_y)
array value. For each contact point there is an associated contact
normal (which is usually the same normal for all points of contact in
the collision). This contact normal is a unit vector that points from
one instance in the collision to another, and can be used, for example,
to calculate the correct "push" direction to resolve collisions **NOTE**
: This variable is only available in the collision event of a physics
enabled instance.

#### Syntax:

``` gml
phy_col_normal_y;
```

#### Returns:

``` gml
 Real

(single precision floating point value, or undefined if the instance is not physics enabled)
```

#### Example:

``` gml
repeat(5 + irandom(5))
{
    with (instance_create_layer(x, y, "Effects", obj_Debris)
    {
        physics_apply_local_impulse(0, 0, other.phy_col_normal_x[0], other.phy_col_normal_y[0]);
    }
}
```

The above code uses the contact normal to set the direction of movement
for an instance created in the collision event between two physics
enabled instances.

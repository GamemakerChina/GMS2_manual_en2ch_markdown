# phy_fixed_rotation

This variable can be used to set whether or not the instance can be
affected by rotational forces (default is false ). If this is set to
true , no external force (either from coded impulses or forces, or from
collisions) will affect the rotation value of the instance and this
would have to be set manually using the [ phy_rotation
](phy_rotation) variable

#### Syntax:

``` gml
phy_fixed_rotation;
```

#### Returns:

``` gml
 Boolean

(or undefined if the instance is not physics enabled)
```

#### Example:

``` gml
phy_rotation = 0; phy_fixed_rotation = true;
```

The above code will switch the instance to have a fixed rotation, then
set the rotation angle.

# phy_bullet

This variable defines whether or not the instance is extremely fast
moving (for example a bullet). The default value is false but if set to
true this tells GameMaker that the instance will be moving at such high
speeds that it will require more expensive collision detection to ensure
it doesn't pass through other instances undetected

#### Syntax:

``` gml
phy_bullet;
```

#### Returns:

``` gml
 Boolean

(or undefined if the instance is not physics enabled)
```

#### Example:

``` gml
with (instance_create_layer(x, y, "Bullets", obj_Shoot))
{
    phy_bullet = true;
    physics_apply_local_impulse(0, 10, 0, 200);
}
```

The above code creates a new instance and then defines it as being a
"bullet" in the physics world before giving it a massive impulse along
the y axis.

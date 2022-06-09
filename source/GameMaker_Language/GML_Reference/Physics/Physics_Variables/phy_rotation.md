# phy_rotation

This variable can be used to get (or to set) the angle of the instances
fixture in degrees, similar to setting or getting the [ image_angle
](../../Asset_Management/Sprites/Sprite_Instance_Variables/image_angle)
. However note that in the physics world rotations are calculated in the
*opposite* way to the normal GameMaker game world, meaning that vector
functions like [ point_direction()
](../../Maths_And_Numbers/Angles_And_Distance/point_direction)
should have their return values modified (simply making positive to
negative should resolve this).

#### Syntax:

``` gml
phy_rotation;
```

#### Returns:

``` gml
 Real

(single precision floating point value, or undefined if the instance is not physics enabled)
```

#### Example:

``` gml
if (phy_speed_x &amp;gt; 0) || (phy_speed_y &amp;gt; 0)
{
    phy_rotation += sqrt(sqr(phy_speed_x) + sqr(phy_speed_y)) /10;
}
```

The above code checks the linear speed and if either vector is not 0, it
then calculates the actual speed and uses that to set the rotation.

# image_speed

This variable determines the speed in which GameMaker will cycle through
the sub-images for the current instance sprite. The speed value given is
a *multiplier* , with 1 being the default value, and setting it to 0.5
will half the animation speed - as set in the [Sprite
Editor](../../../../../The_Asset_Editors/Sprites) or [Image
Editor](../../../../../The_Asset_Editors/Image_Editor) - while
setting it to 2 will double it. If the sprite used has no sub-images,
this variable will have no effect.

#### Syntax:

``` gml
image_speed;
```

#### Returns:

``` gml
 Real

(single precision floating point value)
```

#### Example:

``` gml
with (instance_create_layer(x, y, "Effects", obj_Explosion))
{
    image_speed = 0.5;
}
```

The above code creates an instance of the object "obj_Explosion" and
sets its image_speed to 0.5 (effectively halving the running speed).

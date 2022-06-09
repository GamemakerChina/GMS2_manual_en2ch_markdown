# bbox_top

This **read only** variable returns the position within the room (along
the y-axis) of the top of the bounding box for the instance, where the
bounding box is defined by the maximum width and height of the mask for
the instance (as set by the [sprite_index](sprite_index) or by the
[mask_index](mask_index) ). Even when a sprite has a precise
collision mask, the bounding box exists and is used for certain things,
and so you can use this variable to find it. Please note that when the
instance has no sprite assigned the value returned will be the same as
the instance Y position.

#### Syntax:

``` gml
bbox_top;
```

#### Returns:

``` gml
 Real

(integer)
```

#### Example:

``` gml
if bbox_top &amp;lt; 0
{
    y = sprite_yoffset;
}
```

The above code checks to see if the bounding box of the instance is
outside the room and if it is it sets the instance to a new position.

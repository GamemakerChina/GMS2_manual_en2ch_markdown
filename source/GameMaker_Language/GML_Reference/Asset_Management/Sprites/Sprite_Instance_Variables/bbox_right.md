# bbox_right

This **read only** variable returns the position within the room (along
the x-axis) of the right hand side of the bounding box for the instance,
where the bounding box is defined by the maximum width and height of the
mask for the instance (as set by the [sprite_index](sprite_index) or
by the [mask_index](mask_index) ). Even when a sprite has a precise
collision mask, the bounding box exists and is used for certain things,
and so you can use this variable to find it. Please note that when the
instance has no sprite assigned the value returned will be the same as
the instance X position.

#### Syntax:

``` gml
bbox_right;
```

#### Returns:

``` gml
 Real

(integer)
```

#### Example:

``` gml
if bbox_right &amp;gt; room_width
{
    x = room_width - sprite_xoffset;
}
```

The above code checks to see if the bounding box of the instance is
outside the room and if it is it sets the instance to a new position.

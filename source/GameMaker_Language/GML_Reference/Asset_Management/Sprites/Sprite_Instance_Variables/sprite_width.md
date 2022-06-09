# sprite_width

This **read only** variable returns the width of the sprite that has
been assigned to the instance. This width is returned in pixels and will
be dependent on the [ image_xscale ](image_xscale) . If you need the
un-scaled width you should use [ sprite_get_width()
](../Sprite_Information/sprite_get_width) .

#### Syntax:

``` gml
sprite_width;
```

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
if sprite_width != sprite_get_width(sprite_index)
{
    image_xscale = 1;
}
```

The above code checks the width of the sprite assigned to the instance
running the code against the width of the sprite resource and if it is
not the same, it resets the image_xscale to 1,

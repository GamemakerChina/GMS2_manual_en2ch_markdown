# sprite_height

This **read only** variable returns the height of the sprite that has
been assigned to the instance. This height is returned in pixels and
will be dependent on the [ image_yscale ](image_yscale) . If you
need the un-scaled height you should use [ sprite_get_height()
](../Sprite_Information/sprite_get_height) .

#### Syntax:

``` gml
sprite_height;
```

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
if sprite_height != sprite_get_height(sprite_index)
{
    image_yscale = 1;
}
```

The above code checks the height of the sprite assigned to the instance
running the code against the height of the sprite resource and if it is
not the same, it resets the image_yscale to 1,

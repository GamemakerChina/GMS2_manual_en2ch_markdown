# sprite_get_width

With this function you can find the width of the base resource sprite,
with no transforms, in pixels.

#### Syntax:

``` gml
sprite_get_width(index);
```

|          |                                                                   |                                               |
|----------|-------------------------------------------------------------------|-----------------------------------------------|
| Argument | Type                                                              | Description                                   |
| index    |  [Sprite Asset](../../../../../../The_Asset_Editors/Sprites)  | The index of the sprite to find the width of. |

#### Returns

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

The above code checks the width of the sprite as it is in the current
instance and if there is a difference between that and the original base
sprite, it resets the x axis scale.

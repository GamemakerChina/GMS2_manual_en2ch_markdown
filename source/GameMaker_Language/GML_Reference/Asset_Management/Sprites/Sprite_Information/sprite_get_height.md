# sprite_get_height

With this function you can find the height of the base sprite asset,
with no transforms, in pixels.

#### Syntax:

``` gml
sprite_get_height(index);
```

|          |                                                                   |                                                |
|----------|-------------------------------------------------------------------|------------------------------------------------|
| Argument | Type                                                              | Description                                    |
| index    |  [Sprite Asset](../../../../../../The_Asset_Editors/Sprites)  | The index of the sprite to find the height of. |

#### Returns

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

The above code checks the height of the sprite as it is in the current
instance and if there is a difference between that and the original base
sprite, it resets the y axis scale.

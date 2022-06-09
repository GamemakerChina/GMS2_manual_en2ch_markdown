# sprite_exists

This function returns whether a sprite with the specified index exists
or not in the project being run.

#### Syntax:

``` gml
sprite_exists(index);
```

|          |                                                                   |                                   |
|----------|-------------------------------------------------------------------|-----------------------------------|
| Argument | Type                                                              | Description                       |
| index    |  [Sprite Asset](../../../../../../The_Asset_Editors/Sprites)  | The index of the sprite to check. |

#### Returns

``` gml
N/A
```

#### Example:

``` gml
if sprite_exists(spr_array[0])
{
    sprite_index = spr_array[0];
}
else
{
    sprite_index = spr_BaseSprite;
}
```

The above code checks an array to see if it contains a valid sprite
index and if so it assigns that sprite to the instance, but if not, it
assigns a sprite from the included resources.

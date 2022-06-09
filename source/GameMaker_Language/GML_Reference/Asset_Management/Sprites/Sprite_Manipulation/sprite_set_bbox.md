# sprite_set_bbox

This function can be used to set the bounding box values for a sprite.
You supply the sprite index to use and then the left, top, right and
bottom values for the bounding box positions. The positions are
*absolute* values, where the (0, 0) position corresponds to the top left
corner of the sprite, regardless of the offset for the sprite, any
"empty" pixels the sprite may have, or where it is being drawn in the
room. NOTE This function affects the sprite **asset** so that all
further instances with this sprite will have the same bounding box.

#### Syntax:

``` gml
sprite_set_bbox(ind, left, top, right, bottom);
```

|          |                                                                            |                                                     |
|----------|----------------------------------------------------------------------------|-----------------------------------------------------|
| Argument | Type                                                                       | Description                                         |
| ind      |  [Sprite Asset](../../../../../../The_Asset_Editors/Sprites)           | The index of the sprite to set the bounding box on. |
| left     |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The left side of the bounding box                   |
| top      |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The top of the bounding box.                        |
| right    |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The right side of the bounding box                  |
| bottom   |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The bottom of the bounding box.                     |

#### Returns

``` gml
N/A
```

#### Example:

``` gml
if sprite_get_bbox_mode(sprite_index) == 2
{
    left = irandom(sprite_width / 2);
    right = irandom((sprite_width / 2) + irandom(sprite_width / 2));
    top = irandom(sprite_height / 2);
    bottom = irandom((sprite_height / 2) + irandom(sprite_height / 2));
    sprite_set_bbox(sprite_index, left, top, right, bottom);
}
```

The above code will check the bounding box mode of the sprite assigned
to the sprite_index , and if it is set to manual then it will have its
bounding box changed.

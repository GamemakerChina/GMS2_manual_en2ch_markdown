# sprite_set_bbox_mode

This function can be used to set the bounding box mode for a sprite. You
supply the sprite index and the mode to use, which should be one of the
following constants:

|                                                                                                                                                          |                                                                                                                                                               |
|----------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
|  [Bounding Box Mode Constant](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Sprites/Sprite_Manipulation/sprite_set_bbox_mode)  |                                                                                                                                                               |
| Constant                                                                                                                                                 | Description                                                                                                                                                   |
|  bboxmode_automatic                                                                                                                                      | **Automatic** - The bounding box will be calculated automatically, based on the tolerance setting for the sprite                                              |
|  bboxmode_fullimage                                                                                                                                      | **Full Image** - The bounding box will be set to use the full width and height of the sprite, regardless of the tolerance and "empty" pixels                  |
|  bboxmode_manual                                                                                                                                         | **Manual** - The bounding box is being set manually to user defined values, which requires the use of the function [ sprite_set_bbox() ](sprite_set_bbox) |

NOTE This function affects the sprite **asset** so that all further
instances with this sprite will have the same bounding box mode.

#### Syntax:

``` gml
sprite_set_bbox_mode(ind, mode);
```

|          |                                                                                                                                                          |                                                |
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| Argument | Type                                                                                                                                                     | Description                                    |
| ind      |  [Sprite Asset](../../../../../../The_Asset_Editors/Sprites)                                                                                         | The index of the sprite to change the mode of. |
| mode     |  [Bounding Box Mode Constant](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Sprites/Sprite_Manipulation/sprite_set_bbox_mode)  | The mode to set (a constant).                  |

#### Returns

``` gml
N/A
```

#### Example:

``` gml
if sprite_get_bbox_mode(sprite_index) != bboxmode_automatic
{
    sprite_set_bbox_mode(sprite_index, bboxmode_automatic);
}
```

The above code checks the bbox mode for the current sprite and if it's
not automatic , then it is set to that value.

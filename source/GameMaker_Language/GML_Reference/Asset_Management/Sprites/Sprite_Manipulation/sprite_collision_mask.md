# sprite_collision_mask

With this function you can set the properties of the collision mask that
a sprite should have. If you select either automatic (0) or full image
(1) as the bounding box mode then the individual bounding box values can
be set to 0. However for a user defined mask (2) you will have to set
these values. The different bounding box values are always relative to
the top left corner of the sprite (irrespective of the x and y origin)
which is considered position (0, 0). Setting the kind of mask sets the
general shape for the mask itself, but note that anything other than a
rectangular mask will require more processing power when resolving
collisions, with a subsequent drop in performance. In general, you
should only use mask types other than rectangular when absolutely
necessary. **NOTE** : This function does not permit the **rotated
rectangle** collision mask kind. The kind of mask that can be set will
be one of the following constants:

|                                                                                                                                                                   |                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
|  [Bounding Box Kind (Shape) Constant](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Sprites/Sprite_Manipulation/sprite_collision_mask)  |                                                                                                                                                    |
| Constant                                                                                                                                                          | Description                                                                                                                                        |
|  bboxkind_rectangular                                                                                                                                             | A rectangular (non-rotating) rectangle collision mask shape                                                                                        |
|  bboxkind_ellipse                                                                                                                                                 | An elliptical collision mask shape                                                                                                                 |
|  bboxkind_diamond                                                                                                                                                 | A diamond collision mask shape                                                                                                                     |
|  bboxkind_precise                                                                                                                                                 | A precise collision mask, where the mask will conform to the non-transparent pixels of the sprite, based on the tolerance value given (see below)) |

Finally, tolerance is used to define how precise the precise the mask is
(when used with a "full image" mask, this will have no effect), with a
tolerance of 0 meaning that the mask will follow every single pixel that
has a transparency over 0, while other values will shift the collision
mask perimeter depending on the transparency of the pixels. **NOTE** :
This function is only useful for **bitmap** sprites and will not work
with SWF or JSON (Spine) sprites. **NOTE** : This function will only
work on added sprites or duplicated sprites and **not** directly on
pre-made resources. You can duplicate sprites using the function [
sprite_duplicate() ](sprite_duplicate) .

#### Syntax:

``` gml
sprite_collision_mask(ind, sepmasks, bboxmode, bbleft, bbtop, bbright, bbbottom, kind, tolerance);
```

|           |                                                                                                                                                                   |                                                                                                                 |
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| Argument  | Type                                                                                                                                                              | Description                                                                                                     |
| ind       |  [Sprite Asset](../../../../../../The_Asset_Editors/Sprites)                                                                                                  | The index of the sprite to set the bounding box of.                                                             |
| sepmasks  |  [Boolean](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                                      | Whether to create collision masks for each sub-image of the sprite ( true ), or one mask for all ( false ).     |
| bboxmode  |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                                         | What kind of bounding box to use. 0 = automatic, 1 = full image, 2 = user defined.                              |
| bbleft    |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                                         | The maximum left position of the bounding box.                                                                  |
| bbtop     |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                                         | The maximum top position of the bounding box.                                                                   |
| bbright   |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                                         | The maximum right position of the bounding box.                                                                 |
| bbbottom  |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                                         | The maximum bottom position of the bounding box.                                                                |
| kind      |  [Bounding Box Kind (Shape) Constant](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Sprites/Sprite_Manipulation/sprite_collision_mask)  | The kind of mask, a constant (see the table in the description).                                                |
| tolerance |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                                         | Indicates the tolerance in the transparency value (0=no tolerance, 255=full tolerance).                         |

#### Returns

``` gml
N/A
```

#### Example:

``` gml
spr = sprite_add("player_5.png", 16, true, true, 0, 0);
sprite_collision_mask(spr, true, 1, 0, 0, 0, 0, 0, 0);
```

The above code loads a sprite from an external source and stores the new
index in the variable "spr". The code then sets the new sprite to have a
precise collision mask for each of its sub-images.

# sprite_set_offset

This function can be used to set the x and y origin of a sprite, and
takes relative values based on the (0,0) position being the upper left
corner of the sprite. The following image illustrates this:  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/GML/Reference/Sprites/spr_xyoffset.png)  
** NOTE ** This function affects the sprite **asset** so that all
further instances with this sprite will have the same offset.

#### Syntax:

``` gml
sprite_set_offset(ind, xoff, yoff);
```

|          |                                                                            |                                                  |
|----------|----------------------------------------------------------------------------|--------------------------------------------------|
| Argument | Type                                                                       | Description                                      |
| ind      |  [Sprite Asset](../../../../../../The_Asset_Editors/Sprites)           | The index of the sprite to change the offset of. |
| xoff     |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The x position of the origin.                    |
| yoff     |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The y position of the origin.                    |

#### Returns

``` gml
N/A
```

#### Example:

``` gml
sprite_assign(spr_Custom, spr_Base); sprite_set_offset(spr_Custom, sprite_get_xoffset(spr_Base), sprite_get_yoffset(spr_Base));
```

The above code assigns the sprite indexed in "spr_Base" to the sprite
indexed in "spr_Custom" and then uses the x and y offset values of
"spr_Base" to set the new sprite's origin.

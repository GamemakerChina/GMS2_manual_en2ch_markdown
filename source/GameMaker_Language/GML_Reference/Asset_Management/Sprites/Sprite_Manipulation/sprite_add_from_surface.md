# sprite_add_from_surface

This function works in exactly the same way as [
sprite_create_from_surface() ](sprite_create_from_surface) only
instead of creating a new sprite from the area of the indexed surface
that you select, it adds the defined area of the surface as a new
sub-image to a previously created sprite (this means that you cannot add
it directly to a sprite from the resource tree, but rather only to one
previously created from a surface, or one that has been duplicated from
a resource sprite using [ sprite_duplicate() ](sprite_duplicate) ).
It should be noted that the memory used when adding a sprite in this way
will be larger than you may expect. This is because GameMaker will store
the sprite as a texture page *and* it will also be stored in GPU memory,
so the total memory will be larger than would be expected for an image
file of the same sprite.

#### Syntax:

``` gml
sprite_add_from_surface(index, surface, x, y, w, h, removeback, smooth);
```

|            |                                                                                                        |                                                                                                  |
|------------|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| Argument   | Type                                                                                                   | Description                                                                                      |
| index      |  [Sprite Asset](../../../../../../The_Asset_Editors/Sprites)                                       | The index of the sprite to add the new image to.                                                 |
| surface    |  [Surface ID](../../../../../../GameMaker_Language/GML_Reference/Drawing/Surfaces/surface_create)  | The index of the surface from which we get the image.                                            |
| x          |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                              | The x position to copy from.                                                                     |
| y          |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                              | The y position to copy from.                                                                     |
| w          |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                              | The width of the area to be copied (from the x position).                                        |
| h          |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                              | The height of the area to be copied (from the y position).                                       |
| removeback |  [Boolean](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                           | Indicates whether to make all pixels with the background colour (left-bottom pixel) transparent. |
| smooth     |  [Boolean](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                           | Indicates whether to smooth the edges.                                                           |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
spr_custom = sprite_create_from_surface(surf, 0, 0, 32, 32, true, true, 16, 16);
var i;
for (i = 1; i &amp;lt; 8; i += 1)
{
    sprite_add_from_surface(spr_custom, surf, i, 0, 32, 32, true, true);
}
```

The above code creates a sprite from the surface indexed in the variable
"surf", assigning its index to the variable "spr_Custom", and then uses
a for loop to move across the surface and capture various sections which
are added into the sprite as sub-images.

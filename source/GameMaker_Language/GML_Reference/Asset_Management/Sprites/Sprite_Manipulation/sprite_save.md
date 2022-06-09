# sprite_save

This function can be used to save any sub-image of a sprite to disc,
giving it the specified filename. The sprite must have been
[added](sprite_add) at runtime (you cannot save sprites added
through the IDE) and the file must be saved with a \*.png extension.
**NOTE** : Depending on the target platform that is chosen you are
limited as to where you can save and load files from. See [File
Handling](../../../../../Additional_Information/The_File_System) for
more information.

#### Syntax:

``` gml
sprite_save(ind, subimg, fname);
```

|          |                                                                              |                                      |
|----------|------------------------------------------------------------------------------|--------------------------------------|
| Argument | Type                                                                         | Description                          |
| ind      |  [Sprite Asset](../../../../../../The_Asset_Editors/Sprites)             | The index of the sprite to save.     |
| subimg   |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)    | The sub-image of the sprite to save. |
| fname    |  [String](../../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The filename for the saved sprite.   |

#### Returns

``` gml
N/A
```

#### Example:

``` gml
var surf, spr_custom;
surf = surface_create(32, 32);
surface_set_target(surf);
draw_clear_alpha(c_black, 0);
draw_sprite(spr_Body, 0, 0, 0);
draw_sprite(spr_Clothes, 0, 0, 0);
draw_sprite(spr_Hair, 0, 0, 0);
spr_custom = sprite_create_from_surface(surf, 0, 0, 32, 32, true, true, 16, 16);
surface_reset_target();
surface_free(surf);
sprite_save(spr_custom, 0, "Player_Custom_Sprite.png");
sprite_delete(spr_Custom);
```

The above code creates a surface and stores its index in the local
variable "surf". It then targets that surface, clears it and draws
several sprites on top of each other. It creates a new sprite from the
composite image drawn on the surface and assigns its index to the local
variable "spr_Custom" before freeing up the memory used by the surface.
Finally, the resulting sprite is saved to a file and then removed from
memory too.

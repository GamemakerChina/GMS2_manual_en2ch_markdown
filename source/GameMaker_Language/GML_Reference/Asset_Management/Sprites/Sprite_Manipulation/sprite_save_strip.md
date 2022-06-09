# sprite_save_strip

This function will create a strip image from all the sub-images in a
sprite, saving it to disc with the specified filename. The sprite must
have been [added](sprite_add) at runtime (you cannot save sprites
added through the IDE) and the file must be saved with a \*.png
extension. **NOTE** : Depending on the target platform that is chosen
you are limited as to where you can save and load files from. See [File
Handling](../../../../../Additional_Information/The_File_System) for
more information.

#### Syntax:

``` gml
sprite_save_strip(ind, filename);
```

|          |                                                                              |                                          |
|----------|------------------------------------------------------------------------------|------------------------------------------|
| Argument | Type                                                                         | Description                              |
| ind      |  [Sprite Asset](../../../../../../The_Asset_Editors/Sprites)             | The index of the sprite to save.         |
| filename |  [String](../../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The filename for the saved sprite strip. |

#### Returns

``` gml
N/A
```

#### Example:

``` gml
var spr, i;
spr = sprite_create_from_surface(0, 0, 32, 32, true, true, 16, 16);

for (i = 1; i &amp;lt; 8; i +=1)
{
    sprite_add_from_surface(spr, i, 0, 32, 32, true, true, 16, 16);
}

sprite_save_strip(spr, "Custom_Player_Sprite.png");
sprite_delete(spr);
```

The above code creates a sprite from the surface indexed in the variable
"surf", assigning its index to the local variable "spr_Custom", and then
uses a for loop to move across the surface and capture various sections
which are added into the sprite as sub-images. this new sprite is then
saved as a png strip before being removed from memory.

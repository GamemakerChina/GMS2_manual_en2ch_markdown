# texture_is_ready

This function can be used to check if a specific texture page has been
unpacked and is ready for use, or if a group of texture pages have been
unpacked and are ready for use. You supply the unique **texture page
ID** (as returned by the texturegroup\_\* functions) or the texture
group ID string (as defined in the Texture Group Editor), and the
function will return true if they have been unpacked, or false
otherwise.

#### Syntax:

``` gml
texture_is_ready(tex_id);
```

|          |                                                                                                                                                                                                              |                                                               |
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| Argument | Type                                                                                                                                                                                                         | Description                                                   |
| tex_id   |  [Texture](../../../../../GameMaker_Language/GML_Reference/Asset_Management/Sprites/Sprite_Information/sprite_get_texture) or [String](../../../../../GameMaker_Language/GML_Overview/Data_Types)    | The texture page pointer *or* a texture group name (a string) |

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
var _tex_array = texturegroup_get_textures( "MainMenu");
for (var i = 0; i &amp;lt; array_length(_tex_array); ++i;)
{
    if !texture_is_ready(_tex_array[i])
    {
        texture_prefetch(_tex_array[i]);
    }
}
```

The above code will retrieve the texture page IDs for the texture group
"MainMenu", then check to see if they are unpacked, and if they are not
thenthey are prefetched into VRAM.

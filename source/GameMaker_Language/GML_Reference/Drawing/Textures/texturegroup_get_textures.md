# texturegroup_get_textures

This function can be used to retrieve the **texture page IDs** of the
individual pages that make up a texture group. You supply the texture
group ID string (as defined in the Texture Group Editor), and the
function will return a 1D array, where each entry in the array is a
single texture page ID. If the function fails - ie: an invalid group is
given, or the group has no texture assigned to it - then the array will
be empty (0 length).

#### Syntax:

``` gml
texturegroup_get_textures(tex_id);
```

|          |                                                                           |                                                   |
|----------|---------------------------------------------------------------------------|---------------------------------------------------|
| Argument | Type                                                                      | Description                                       |
| tex_id   |  [String](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The name of the texture group to check (a string) |

#### Returns:

``` gml
 Array

of

 Texture

s
```

#### Example:

``` gml
var _tex_array = texturegroup_get_textures( "MainMenu");
for (var i = 0; i &amp;lt; array_length(_tex_array); ++i;)
{
    if texture_is_ready(_tex_array[i])
    {
        texture_prefetch(_tex_array[i]);
    }
}
```

The above code will retrieve the texture page IDs for the texture group
"MainMenu", then check to see if they are unpacked, and if they are them
they are placed into VRAM.

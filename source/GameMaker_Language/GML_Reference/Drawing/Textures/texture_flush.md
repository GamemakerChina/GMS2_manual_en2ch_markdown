# texture_flush

This function can be used to "flush" a texture page or a group of
texture pages, ie: remove them from VRAM when no longer required. You
supply the unique **texture page ID** (as returned by the
texturegroup\_\* functions) to flush a single page, or you can supply a
**texture group name** (as defined in the [Texture Group
Editor](../../../../Settings/Texture_Groups) ) to flush all the
texture pages in the group.

#### Syntax:

``` gml
texture_flush(tex_id);
```

|          |                                                                                                                                                                                                              |                                                               |
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| Argument | Type                                                                                                                                                                                                         | Description                                                   |
| tex_id   |  [Texture](../../../../../GameMaker_Language/GML_Reference/Asset_Management/Sprites/Sprite_Information/sprite_get_texture) or [String](../../../../../GameMaker_Language/GML_Overview/Data_Types)    | The texture page pointer *or* a texture group name (a string) |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
var _tex_array = texturegroup_get_textures( "MainMenu");
for (var i = 0; i &amp;lt; array_length(_tex_array); ++i;)
{
    texture_flush(_tex_array[i]);
}
```

The above code will flush all the texture pages under the texture group
"MainMenu".

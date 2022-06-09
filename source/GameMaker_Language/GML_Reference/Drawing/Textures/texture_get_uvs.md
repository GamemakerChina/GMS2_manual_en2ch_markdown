# texture_get_uvs

This function returns a 1D [array](../../../GML_Overview/Arrays)
with 4 elements representing the UV coordinates for the given texture
pointer, filling in the array with the following values:

-   \[0\] = left
-   \[1\] = top
-   \[2\] = right
-   \[3\] = bottom
-   \[4\] = amount of pixels the asset compiler has trimmed from the
    sprites left side (sprite assets only)
-   \[5\] = amount of pixels the asset compiler has trimmed from the
    sprites top side (sprite assets only)
-   \[6\] = normalised percentage of pixel data from the original
    sprites width that has been saved to the texture page (sprite assets
    only)
-   \[7\] = normalised percentage of pixel data from the original
    sprites height that has been saved to the texture page (sprite
    assets only)

This value can then be used in other draw functions, particularly in
general 3D and some of the 2D primitive functions, as well as the Shader
functions. If you need the UVS for a sprite then you can use the
[sprite_get_uvs()](../../Asset_Management/Sprites/Sprite_Information/sprite_get_uvs)
and for a font, [ font_get_uvs()
](../../Asset_Management/Fonts/font_get_uvs) .

#### Syntax:

``` gml
texture_get_uvs(texid)
```

|          |                                                                                                                                 |                                        |
|----------|---------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| Argument | Type                                                                                                                            | Description                            |
| texid    |  [Texture](../../../../../GameMaker_Language/GML_Reference/Asset_Management/Sprites/Sprite_Information/sprite_get_texture)  | The texture pointer to get the UVS for |

#### Returns:

``` gml
 Array

(4 - 8 elements)
```

#### Example:

``` gml
var _tex = surface_get_texture(surf_back);
var _uvs = texture_get_uvs(tex);
var _uvs_left = _uvs[0];
var _uvs_top = _uvs[1];
var _uvs_right = _uvs[2];
var _uvs_bottom = _uvs[3];
```

The above code first retrieves the texture for the surface stored in
surf_back , and then gets the UV coordinates for that texture. It then
retrieves the left, top, right and bottom UV coordinates from the
returned array and stores them in local variables.

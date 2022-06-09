# sprite_get_uvs

This function returns an [array](../../../../GML_Overview/Arrays)
with the UV coordinates and other data for the texture of the sprite
sub-image on the texture page. The function returns an array with the
following 8 elements:

-   \[0\] = left
-   \[1\] = top
-   \[2\] = right
-   \[3\] = bottom
-   \[4\] = amount of pixels the asset compiler has trimmed from the
    sprites left side
-   \[5\] = amount of pixels the asset compiler has trimmed from the
    sprites top side
-   \[6\] = normalised percentage of pixel data from the original
    sprites width that has been saved to the texture page
-   \[7\] = normalised percentage of pixel data from the original
    sprites height that has been saved to the texture page

This array can then be used in other draw functions, particularly when
working in 3D or using the [2D
primitive](../../../Drawing/Primitives/Primitives_And_Vertex_Formats)
functions, as well as when working with the
[Shader](../../Shaders/Shaders) functions. **NOTE** : This function
will **not** work with vector sprites or skeleton animation sprites.

#### Syntax:

``` gml
sprite_get_uvs(sprite, subimage);
```

|          |                                                                            |                                     |
|----------|----------------------------------------------------------------------------|-------------------------------------|
| Argument | Type                                                                       | Description                         |
| sprite   |  [Sprite Asset](../../../../../../The_Asset_Editors/Sprites)           | The index of the sprite to use.     |
| subimage |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The sub-image of the sprite to use. |

#### Returns

``` gml
 Array

(1D, 8 elements)
```

#### Example:

``` gml
var tex = sprite_get_uvs(sprite, 0); tex_left = tex[0]; tex_top = tex[1]; tex_right = tex[2]; tex_bottom = tex[3];
```

The above code will store the UV coordinates for the given sprite in a
local array and then assign the values to instance variables.

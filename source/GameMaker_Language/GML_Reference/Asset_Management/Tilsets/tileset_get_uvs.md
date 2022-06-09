# tileset_get_uvs

This function returns an [array](../../../GML_Overview/Arrays) with
the UV coordinates and other data for the texture of the given tile set
on the texture page. The function returns an array with the following 8
elements:

-   \[0\] = left
-   \[1\] = top
-   \[2\] = right
-   \[3\] = bottom
-   \[4\] = amount of pixels the asset compiler has trimmed from the
    tile set left side
-   \[5\] = amount of pixels the asset compiler has trimmed from the
    tile set top side
-   \[6\] = normalised percentage of pixel data from the original tile
    set width that has been saved to the texture page
-   \[7\] = normalised percentage of pixel data from the original tile
    set height that has been saved to the texture page

This array can then be used in other draw functions, particularly when
working in 3D or using the [2D
primitive](../../Drawing/Primitives/Primitives_And_Vertex_Formats)
functions, as well as when working with the
[Shader](../Shaders/Shaders) functions.

#### Syntax:

``` gml
tileset_get_uvs(tileset);
```

|          |                                                                    |                                   |
|----------|--------------------------------------------------------------------|-----------------------------------|
| Argument | Type                                                               | Description                       |
| tileset  |  [Tile Set Asset](../../../../../The_Asset_Editors/Tile_Sets)  | The index of the tile set to use. |

#### Returns

``` gml
 Array

(1D, 8 elements)
```

#### Example:

``` gml
var tex = tileset_get_uvs(tl_Grass); tex_left = tex[0]; tex_top = tex[1]; tex_right = tex[2]; tex_bottom = tex[3];
```

The above code will store the UV coordinates for the given tile set in a
local array and then assign the values to instance variables.

# font_get_uvs

This function returns an [array](../../../GML_Overview/Arrays) with
the UV coordinates for the font texture on the texture page, filling in
the array with the following values:

-   \[0\] = left
-   \[1\] = top
-   \[2\] = right
-   \[3\] = bottom

This value can then be used in other draw functions, particularly in
general drawing when using
[primitives](../../Drawing/Primitives/Primitives_And_Vertex_Formats)
as well as the [Shader](../Shaders/Shaders) functions.

#### Syntax:

``` gml
font_get_uvs(font);
```

|          |                                                            |                               |
|----------|------------------------------------------------------------|-------------------------------|
| Argument | Type                                                       | Description                   |
| font     |  [Font Asset](../../../../../The_Asset_Editors/Fonts)  | The index of the font to use. |

#### Returns:

``` gml
 Array
```

#### Example:

``` gml
var tex = font_get_uvs(fnt_Main); tex_left = tex[0]; tex_top = tex[1]; tex_right = tex[2]; tex_left = tex[3];
```

The above code will store the UV coordinates for the given background in
a local array and then assign the values to instance variables.

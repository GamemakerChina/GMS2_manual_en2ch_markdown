# font_get_texture

This function returns a special *pointer* for the font texture page.
This value can then be used in other draw functions, particularly in
general drawing when using
[primitives](../../Drawing/Primitives/Primitives_And_Vertex_Formats)
as well as the [Shader](../Shaders/Shaders) functions. You can get
more information about the returned texture page using the different
texture\_ functions found [here](../../Drawing/Textures/Textures) .
NOTE On HTML5, this returns a struct instead of a texture pointer, as a
pointer cannot be used on that platform. However this does not change
the use of the returned value, as its usage in [texture
functions](../../Drawing/Textures/Textures) still remains the same.

#### Syntax:

``` gml
font_get_texture(font);
```

|          |                                                            |                               |
|----------|------------------------------------------------------------|-------------------------------|
| Argument | Type                                                       | Description                   |
| font     |  [Font Asset](../../../../../The_Asset_Editors/Fonts)  | The index of the font to use. |

#### Returns:

``` gml
 Texture
```

#### Example:

``` gml
tex = font_get_texture(fnt_Main);
```

The above code will get the texture pointer for the font indexed as
"fnt_Main".

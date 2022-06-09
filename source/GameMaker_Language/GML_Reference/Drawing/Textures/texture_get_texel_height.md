# texture_get_texel_height

A texel, or *texture element* is the fundamental unit of texture space
used in computer graphics. Textures are represented by arrays of texels,
just as pictures are represented by arrays of pixels, and this function
returns the height of a single texel from the texture page of the image
asset used.

#### Syntax:

``` gml
texture_get_texel_height(tex);
```

|          |                                                                                                                                 |                                       |
|----------|---------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| Argument | Type                                                                                                                            | Description                           |
| tex      |  [Texture](../../../../../GameMaker_Language/GML_Reference/Asset_Management/Sprites/Sprite_Information/sprite_get_texture)  | The texture page asset pointer to use |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
var tex = sprite_get_texture(sprite_index, 0);
tex_w = texture_get_texel_width(tex);
tex_h = texture_get_texel_height(tex);
```

The above code will get the texel width and height of the texture taken
from a sprite asset.

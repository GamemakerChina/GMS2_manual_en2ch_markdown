# texture_get_width

Returns the width of the texture with the given id, which is always a
value within the range 0 - 1. This can then be used when mapping
textures to models or primitives.

#### Syntax:

``` gml
texture_get_width(tex);
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
tex_w = texture_get_width(sprite_get_texture(spr_Model_tex, 0));
```

The above code will get the width of the texture taken from a sprite
asset.

# texture_get_height

Returns the height of the texture with the given id, which is always a
value within the range 0 - 1. This can then be used when mapping
textures to models or primitives.

#### Syntax:

``` gml
texture_get_height(tex);
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
tex_h = texture_get_height(surface_get_texture(global.Surf));
```

The above code will get the height of the texture taken from a
previously created surface.

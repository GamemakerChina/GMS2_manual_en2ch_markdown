# texture_set_stage

This function will set the given stage "slot" a texture to be used. The
number of stage "slots" available will depend on the platform you are
compiling to, with a maximum of 8 being available for Windows, Mac and
Linux, but on lower end Android devices (for example) this number can be
as low as 2. It is also worth noting that the first stage slot (1) is
always used automatically by GameMaker . **NOTE** : This function will
do nothing outside of the context of a running shader! See
[Shaders](../../Asset_Management/Shaders/Shaders) for more
information.

#### Syntax:

``` gml
texture_set_stage(stage, tex);
```

|          |                                                                                                                                 |                            |
|----------|---------------------------------------------------------------------------------------------------------------------------------|----------------------------|
| Argument | Type                                                                                                                            | Description                |
| stage    |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                          | The texture "slot" to use. |
| tex      |  [Texture](../../../../../GameMaker_Language/GML_Reference/Asset_Management/Sprites/Sprite_Information/sprite_get_texture)  | The texture to use.        |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
glassshader_bgsampler = shader_get_sampler_index(GlassShader, "s_BackgroundSampler")
spr = sprite_get_texture(sprite_index, 0);
shader_set(GlassShader);
texture_set_stage(glassshader_bgsampler, spr);
shader_reset();
```

The above code will get the *handle* for the sampler within the shader
indexed as "GlassShader" and then set that shader constant to the given
sprite texture.

# gpu_set_texrepeat_ext

This function can be used to set whether a single sampler "slot" repeats
the given texture when using
[Shaders](../../Asset_Management/Shaders/Shaders) in GameMaker .
Setting it to true will repeat the texture if the uv coordinates are out
with the 0-1 range, while a setting of false will mean no repeating. The
likely use case for these functions is for repeating a texture in 3D but
in order for it to work and not pull images from the rest of the texture
page, the sprite used will need to be marked as being on a "Separate
Texture Page" in the Sprite Editor. ** NOTE ** This setting will be
over-ridden by the value set when calling the function [
gpu_set_texrepeat() ](gpu_set_texrepeat) .

#### Syntax:

``` gml
gpu_set_texrepeat_ext(sampler_id, enable);
```

|            |                                                                                                                                  |                                                          |
|------------|----------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| Argument   | Type                                                                                                                             | Description                                              |
| sampler_id |  [Shader Sampler Handle](../../../../../GameMaker_Language/GML_Reference/Asset_Management/Shaders/shader_get_sampler_index)  | The sampler id from the shader.                          |
| enable     |  [Boolean](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                        | Enable or disable texture filtering ( true / false )     |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
var s_tex = shader_get_sampler_index(shader_glass, "s_NoiseSampler");
if gpu_get_texfilter_ext(s_tex)
{
    gpu_set_texfilter_ext(s_tex, false);
}
else
{
    gpu_set_texfilter_ext(s_tex, true);
}
```

The above code checks to see if texture filtering is on or off for a
specific sampler ID (stored in a local variable) and switches it
accordingly.

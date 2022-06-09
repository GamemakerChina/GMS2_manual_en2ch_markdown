# gpu_set_tex_mip_bias_ext

With this function you can set the mipmap bias value for a given shader
sampler. You supply the index value for the shader sampler (as returned
by the function [ shader_get_sampler_index()
](../../Asset_Management/Shaders/shader_get_sampler_index) , and
then the bias value, where 0 is for no bias, 1 equals the first mipmap,
2 equals the second mipmap etc... This controls the rate at which the
mip map is swapped and will generally make the shader textures blurrier
the higher the value and the greater the "distance" being viewed. Note
that this function can also take negative values too, in which case
shader textures will be sharper over a greater distance the lower the
value.

#### Syntax:

``` gml
gpu_set_tex_mip_bias_ext(sampler_index, bias);
```

|               |                                                                                                                                  |                                           |
|---------------|----------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------|
| Argument      | Type                                                                                                                             | Description                               |
| sampler_index |  [Shader Sampler Handle](../../../../../GameMaker_Language/GML_Reference/Asset_Management/Shaders/shader_get_sampler_index)  | The index of the shader sampler to get    |
| bias          |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                           | The mipmap bias value to use (default: 0) |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
var _sampleIndex = shader_get_sampler_index(shd_Glass, "s_Background");
var _spriteTex = sprite_get_texture(sprite_index, 0);
shader_set(shd_Glass);
if gpu_get_tex_mip_bias_ext(_sampleIndex) != 0
{
    gpu_set_tex_mip_bias_ext(_sampleIndex, 0);
}
texture_set_stage(_sampleIndex , _spriteTex);
shader_reset();
```

The above code sets the mip filter bias to 0 for the given shader
texture sampler if it has not already been set to 0.

# gpu_get_tex_mip_bias_ext

With this function you can retrieve the mipmap bias value for a given
shader sampler. You supply the index value for the shader sampler (as
returned by the function [ shader_get_sampler_index()
](../../Asset_Management/Shaders/shader_get_sampler_index) , and the
function will return a value of 0.0 for no bias, or a greater value
where 1 equals the first mipmap, 2 equals the second mipmap etc... This
controls the rate at which the mip map is swapped and will generally
make the shader textures blurrier the higher the value and the greater
the "distance" being viewed. Note that this can return negative values
too, in which case shader textures will be sharper over a greater
distance the lower the value.

#### Syntax:

``` gml
gpu_get_tex_mip_bias_ext(sampler_index);
```

|               |                                                                                                                                  |                                        |
|---------------|----------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| Argument      | Type                                                                                                                             | Description                            |
| sampler_index |  [Shader Sampler Handle](../../../../../GameMaker_Language/GML_Reference/Asset_Management/Shaders/shader_get_sampler_index)  | The index of the shader sampler to get |

#### Returns:

``` gml
 Real

(default: 0)
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

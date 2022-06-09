# gpu_get_tex_max_aniso_ext

With this function you can get the current maximum level of anisotropy
when using the tf_anisotropic filter mode (see [
gpu_get_tex_mip_filter() ](gpu_get_tex_mip_filter) for more
information) on a shader sampler. You supply the index value for the
shader sampler (as returned by the function [ shader_get_sampler_index()
](../../Asset_Management/Shaders/shader_get_sampler_index) , and the
function will return a value within the range of 1 and 16.

#### Syntax:

``` gml
gpu_get_tex_max_aniso_ext(sampler_index);
```

|               |                                                                                                                                  |                                        |
|---------------|----------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| Argument      | Type                                                                                                                             | Description                            |
| sampler_index |  [Shader Sampler Handle](../../../../../GameMaker_Language/GML_Reference/Asset_Management/Shaders/shader_get_sampler_index)  | The index of the shader sampler to get |

#### Returns:

``` gml
 Real

(default: 16)
```

#### Example:

``` gml
var _sampleIndex = shader_get_sampler_index(shd_Glass, "s_Background");
var _spriteTex = sprite_get_texture(sprite_index, 0);
shader_set(shd_Glass);
if gpu_get_tex_max_aniso_ext(_sampleIndex) != 8
{
    gpu_set_tex_max_aniso_ext(_sampleIndex, 8);
}
texture_set_stage(_sampleIndex , _spriteTex);
shader_reset();
```

The above code sets the maximum level of anisotropy to 8 for the given
shader texture sampler if it has not already been set to 8.

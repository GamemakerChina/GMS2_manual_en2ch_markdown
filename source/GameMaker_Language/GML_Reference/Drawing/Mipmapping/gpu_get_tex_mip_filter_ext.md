# gpu_get_tex_mip_filter_ext

With this function you can get the current mip filter mode for a given
shader sampler. You supply the index value for the shader sampler (as
returned by the function [ shader_get_sampler_index()
](../../Asset_Management/Shaders/shader_get_sampler_index) , and the
function will return one of the mode value constants listed below.

#### Syntax:

``` gml
gpu_get_tex_mip_filter_ext(sampler_index);
```

|               |                                                                                                                                  |                                        |
|---------------|----------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| Argument      | Type                                                                                                                             | Description                            |
| sampler_index |  [Shader Sampler Handle](../../../../../GameMaker_Language/GML_Reference/Asset_Management/Shaders/shader_get_sampler_index)  | The index of the shader sampler to get |

#### Returns:

``` gml
 Mipmapping Filter Constant

(listed below):
```

|                |                                                                                                                                                                                                                |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Constant       | Description                                                                                                                                                                                                    |
| tf_point       | This means that blending between mipmap levels is disabled, which can cause visible texture transitions, but gives the best performance.                                                                       |
| tf_linear      | This means that blending between mipmap levels is enabled (this is also known as *trilinear filtering* ), which smooths the texture transitions, but it will give a minor hit to performance.                  |
| tf_anisotropic | This means that anisotropic filtering is enabled, which greatly improves texture transition quality and can reduce the blurring visible with other filtering modes, but it has the highest hit on performance. |

#### Example:

``` gml
var _sampleIndex = shader_get_sampler_index(shd_Glass, "s_Background");
var _spriteTex = sprite_get_texture(sprite_index, 0);
shader_set(shd_Glass);
if gpu_get_tex_mip_filter_ext(_sampleIndex) != tf_point
{
    gpu_set_tex_mip_filter_ext(_sampleIndex, tf_point);
}
texture_set_stage(_sampleIndex , _spriteTex);
shader_reset();
```

The above code sets the mip filter mode to tf_point (disabling
mipmapping) for the given shader texture sampler if it has not already
been set.

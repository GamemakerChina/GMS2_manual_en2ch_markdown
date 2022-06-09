# gpu_get_texfilter_ext

With this function you can check to see whether texture interpolation
(linear interpolation) is enabled (returns true ) or not (returns false
) for a given shader sampler texture. **NOTE** : On the HTML5 target,
this function will only work with WebGL enabled.

#### Syntax:

``` gml
gpu_get_texfilter_ext(sampler_id);
```

|            |                                                                                                                                  |                                 |
|------------|----------------------------------------------------------------------------------------------------------------------------------|---------------------------------|
| Argument   | Type                                                                                                                             | Description                     |
| sampler_id |  [Shader Sampler Handle](../../../../../GameMaker_Language/GML_Reference/Asset_Management/Shaders/shader_get_sampler_index)  | The sampler id from the shader. |

#### Returns:

``` gml
 Boolean
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

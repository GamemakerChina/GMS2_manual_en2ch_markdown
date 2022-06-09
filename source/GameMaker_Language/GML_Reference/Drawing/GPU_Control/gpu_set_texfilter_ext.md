# gpu_set_texfilter_ext

This function can be used to set the linear interpolation for a single
sampler "slot" when using
[Shaders](../../Asset_Management/Shaders/Shaders) in GameMaker .
When this is enabled ( true ) the sampler texture will be smoothed and
if this is disabled ( false ) then images will be drawn based on the
nearest pixel. The default value is that set by the **Global Game
Options** for your game, or that set using the function [
gpu_set_texfilter() ](gpu_set_texfilter) . **NOTE** : This setting
will be over-ridden by the value set when calling the function [
gpu_set_texfilter() ](gpu_set_texfilter) . **NOTE** : On the HTML5
target, this function will only work with WebGL enabled.

#### Syntax:

``` gml
gpu_set_texfilter_ext(sampler_id, enable);
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

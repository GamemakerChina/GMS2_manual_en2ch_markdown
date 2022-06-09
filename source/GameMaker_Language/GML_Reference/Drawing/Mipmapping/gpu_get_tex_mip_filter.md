# gpu_get_tex_mip_filter

With this function you can get the current mip filter mode. The mode
value returned by the function will be one of the constants listed
below.

#### Syntax:

``` gml
gpu_get_tex_mip_filter();
```

#### Returns:

``` gml
 Mipmapping Filter Constant

(listed below):
```

|                                                                                                                               |                                                                                                                                                                                                                |
|-------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|  [Mipmapping Filter Constant](../../../../../GameMaker_Language/GML_Reference/Drawing/Mipmapping/gpu_set_tex_mip_filter)  |                                                                                                                                                                                                                |
| Constant                                                                                                                      | Description                                                                                                                                                                                                    |
|  tf_point                                                                                                                     | This means that blending between mipmap levels is disabled, which can cause visible texture transitions, but gives the best performance.                                                                       |
|  tf_linear                                                                                                                    | This means that blending between mipmap levels is enabled (this is also known as *trilinear filtering* ), which smooths the texture transitions, but it will give a minor hit to performance.                  |
|  tf_anisotropic                                                                                                               | This means that anisotropic filtering is enabled, which greatly improves texture transition quality and can reduce the blurring visible with other filtering modes, but it has the highest hit on performance. |

#### Example:

``` gml
if keyboard_check(vk_enter)
{
    switch(gpu_get_tex_mip_filter())
    {
        case tf_point: gpu_set_tex_mip_filter(tf_linear); break;
        case tf_linear: gpu_set_tex_mip_filter(tf_anisotropic); break;
        case tf_anisotropic: gpu_set_tex_mip_filter(tf_point); break;
    }
}
```

The above code checks the keyboard and if the specified key is pressed
it will then get the current mip filter and toggle the value to the next
one, cycling through the different modes.

# gpu_set_tex_mip_filter

With this function you can set the current mip filter mode to one of the
three types supported. You give the constant that refers to the mip
filtering mode that you require, where you can choose between **point**
filtering (default setting, meaning no filtering), **linear** filtering
(this is also known as *trilinear filtering* ) or **aniostropic**
filtering (see the constants table below).

|                  |                                                                                                                                                                                                                            |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Constant         | Description                                                                                                                                                                                                                |
|  tf_point        | This will disable the filtering between mipmap levels, which can cause visible texture transitions, but gives the best performance.                                                                                        |
|  tf_linear       | This will enable linear filtering between mipmap levels (this is also known as *trilinear filtering* ), which smooths the texture transitions, but it will give a minor hit to performance.                                |
|  tf_anisotropic  | This will enable anisotropic filtering between mipmap levels, which greatly improves texture transition quality and can reduce the blurring visible with other filtering modes, but it has the highest hit on performance. |

#### Syntax:

``` gml
gpu_set_tex_mip_filter(filter);
```

|          |                                                                                                                               |                                                                |
|----------|-------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| Argument | Type                                                                                                                          | Description                                                    |
| filter   |  [Mipmapping Filter Constant](../../../../../GameMaker_Language/GML_Reference/Drawing/Mipmapping/gpu_set_tex_mip_filter)  | The mip filter mode to use (a constant, default: tf_point ).   |

#### Returns:

``` gml
N/A
```

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

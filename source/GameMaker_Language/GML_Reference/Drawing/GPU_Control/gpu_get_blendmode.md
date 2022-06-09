# gpu_get_blendmode

This function can be used to retrieve the current blend mode being used
for drawing. The returned value will be one of the following constants
(the default value is bm_normal ):

|                                                                                                                    |                                                                        |                                          |
|--------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|------------------------------------------|
|  [Blend Mode Constant](../../../../../GameMaker_Language/GML_Reference/Drawing/GPU_Control/gpu_get_blendmode)  |                                                                        |                                          |
| Constant                                                                                                           | Description                                                            | Extended Blend Mode                      |
|  bm_normal                                                                                                         | Normal blending (the default blend mode).                              | ( bm_src_alpha , bm_inv_src_alpha )      |
|  bm_add                                                                                                            | Additive blending. Luminosity values of light areas are added.         | ( bm_src_alpha , bm_one )                |
|  bm_subtract                                                                                                       | Subtractive blending. Luminosity values of light areas are subtracted. | ( bm_zero , bm_inv_src_colour )          |
|  bm_max                                                                                                            | Max blending. Similar to additive blending.                            | ( bm_src_alpha , bm_inv_src_colour )     |

#### Syntax:

``` gml
gpu_get_blendmode();
```

#### Returns:

``` gml
 Blend Mode Constant

(see above for constants)
```

#### Example:

``` gml
if gpu_get_blendmode() != bm_normal
{
    gpu_set_blendmode(bm_normal);
}
```

The above code gets the current blend mode and if it is not bm_normal it
is set to that constant.

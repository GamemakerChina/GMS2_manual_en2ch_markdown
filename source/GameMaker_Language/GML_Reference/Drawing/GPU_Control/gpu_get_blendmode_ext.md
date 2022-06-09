# gpu_get_blendmode_ext

This function can be used to retrieve the current extended blend mode
being used for drawing. The function returns a 2 element 1D array with
the following elements in it:

-   \[0\] = Source [Blend Mode Factor
    Constant](../../../../../GameMaker_Language/GML_Reference/Drawing/GPU_Control/gpu_get_blendmode_ext)
    (default is bm_src_alpha )
-   \[1\] = Destination [Blend Mode Factor
    Constant](../../../../../GameMaker_Language/GML_Reference/Drawing/GPU_Control/gpu_get_blendmode_ext)
    (default is bm_inv_src_alpha )

The values of the array will be one of the following constants ("s"
denotes a value taken from the source while a "d" denotes a value from
the destination):

|                                                                                                                               |                                        |
|-------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
|  [Blend Mode Factor Constant](../../../../../GameMaker_Language/GML_Reference/Drawing/GPU_Control/gpu_get_blendmode_ext)  |                                        |
| Constant                                                                                                                      | Blend factor (Red, Green, Blue, Alpha) |
|  bm_zero                                                                                                                      | (0, 0, 0, 0)                           |
|  bm_one                                                                                                                       | (1, 1, 1, 1)                           |
|  bm_src_colour                                                                                                                | (Rs, Gs, Bs, As)                       |
|  bm_inv_src_colour                                                                                                            | (1-Rs, 1-Gs, 1-Bs, 1-As)               |
|  bm_src_alpha                                                                                                                 | (As, As, As, As)                       |
|  bm_inv_src_alpha                                                                                                             | (1-As, 1-As, 1-As, 1-As)               |
|  bm_dest_alpha                                                                                                                | (Ad, Ad, Ad, Ad)                       |
|  bm_inv_dest_alpha                                                                                                            | (1-Ad, 1-Ad, 1-Ad, 1-Ad)               |
|  bm_dest_colour                                                                                                               | (Rd, Gd, Bd, Ad)                       |
|  bm_inv_dest_colour                                                                                                           | (1-Rd, 1-Gd, 1-Bd, 1-Ad)               |
|  bm_src_alpha_sat                                                                                                             | (f, f, f, 1) where f = min(As, 1-Ad)   |

Note that you can change these values and pass the full array to the [
gpu_set_blendmode_ext() ](gpu_set_blendmode_ext) function as a
single argument.

#### Syntax:

``` gml
gpu_get_blendmode_ext();
```

#### Returns:

``` gml
 Array

(2 elements only; see above for constants)
```

#### Example:

``` gml
var bm = gpu_get_blendmode_ext();
bm[0] = bm_src_alpha;
gpu_set_blendmode_ext(bm);
```

The above code gets the current extended blend mode, modifies the
source, and then sets the extended blend mode again.

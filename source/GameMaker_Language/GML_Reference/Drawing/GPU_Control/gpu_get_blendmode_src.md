# gpu_get_blendmode_src

This function can be used to retrieve the current *source* extended
blend mode factor being used for drawing. The value returned will be one
of the following constants ("s" denotes a value taken from the source
while a "d" denotes a value from the destination):

|                      |                                        |
|----------------------|----------------------------------------|
| Constant             | Blend factor (Red, Green, Blue, Alpha) |
|  bm_zero             | (0, 0, 0, 0)                           |
|  bm_one              | (1, 1, 1, 1)                           |
|  bm_src_colour       | (Rs, Gs, Bs, As)                       |
|  bm_inv_src_colour   | (1-Rs, 1-Gs, 1-Bs, 1-As)               |
|  bm_src_alpha        | (As, As, As, As)                       |
|  bm_inv_src_alpha    | (1-As, 1-As, 1-As, 1-As)               |
|  bm_dest_alpha       | (Ad, Ad, Ad, Ad)                       |
|  bm_inv_dest_alpha   | (1-Ad, 1-Ad, 1-Ad, 1-Ad)               |
|  bm_dest_colour      | (Rd, Gd, Bd, Ad)                       |
|  bm_inv_dest_colour  | (1-Rd, 1-Gd, 1-Bd, 1-Ad)               |
|  bm_src_alpha_sat    | (f, f, f, 1) where f = min(As, 1-Ad)   |

#### Syntax:

``` gml
gpu_get_blendmode_src();
```

#### Returns:

``` gml
 Blend Mode Factor Constant

(see above table)
```

#### Example:

``` gml
var bm;
bm[0] = gpu_get_blendmode_src();
bm[1] = gpu_get_blendmode_dest();
gpu_set_blendmode_ext_sepalpha(bm[0], bm[1], bm_inv_src_alpha, bm_inv_dest_colour);
```

The above code creates a local array and gets the current source and
destination blending factors. This array is then used to manipulate the
alpha component of the blending factors.

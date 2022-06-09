# gpu_set_zfunc

This function can be used to set the z-buffer testing comparison mode
(see [ gpu_set_ztestenable() ](gpu_set_ztestenable) for more
information). The values available for use are any of the following
constants (the default value is cmpfunc_lessequal ):

|                        |                  |
|------------------------|------------------|
| Constant               | Description      |
|  cmpfunc_never         | Never            |
|  cmpfunc_less          | Less             |
|  cmpfunc_equal         | Equal            |
|  cmpfunc_lessequal     | Less or Equal    |
|  cmpfunc_greater       | Greater          |
|  cmpfunc_notequal      | Not Equal        |
|  cmpfunc_greaterequal  | Greater or Equal |
|  cmpfunc_always        | Always           |

#### Syntax:

``` gml
gpu_set_zfunc(cmp_func);
```

|          |                                                                                                                         |                                             |
|----------|-------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| Argument | Type                                                                                                                    | Description                                 |
| cmp_func |  [Comparison Function Constant](../../../../../GameMaker_Language/GML_Reference/Drawing/GPU_Control/gpu_get_zfunc)  | The comparison mode to use (see list above) |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
gpu_set_ztestenable(true);
gpu_set_zfunc(cmpfunc_always);
draw_sprite(spr_Background, 0, 0, 0);
gpu_set_ztestenable(false);
```

The above code switches on z-buffer testing and sets its comparison mode
before drawing a background sprite and then switches it back off again
to continue drawing.

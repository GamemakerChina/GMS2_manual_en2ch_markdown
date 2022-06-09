# gpu_get_zfunc

This function can be used to retrieve the z comparison mode. The value
returned will be one of the following constants (the default value is
cmpfunc_lessequal ):

|                                                                                                                         |                  |
|-------------------------------------------------------------------------------------------------------------------------|------------------|
|  [Comparison Function Constant](../../../../../GameMaker_Language/GML_Reference/Drawing/GPU_Control/gpu_get_zfunc)  |                  |
| Constant                                                                                                                | Description      |
|  cmpfunc_never                                                                                                          | Never            |
|  cmpfunc_less                                                                                                           | Less             |
|  cmpfunc_equal                                                                                                          | Equal            |
|  cmpfunc_lessequal                                                                                                      | Less or Equal    |
|  cmpfunc_greater                                                                                                        | Greater          |
|  cmpfunc_notequal                                                                                                       | Not Equal        |
|  cmpfunc_greaterequal                                                                                                   | Greater or Equal |
|  cmpfunc_always                                                                                                         | Always           |

#### Syntax:

``` gml
gpu_get_zfunc();
```

#### Returns:

``` gml
 Comparison Function Constant

(see table above)
```

#### Example:

``` gml
if gpu_get_zfunc() != cmpfunc_greater
{
    gpu_set_zfunc(cmpfunc_greater);
}
```

The above code checks to see if the z-testing method is set to
cmpfunc_greater and if not then it is set to that constant.

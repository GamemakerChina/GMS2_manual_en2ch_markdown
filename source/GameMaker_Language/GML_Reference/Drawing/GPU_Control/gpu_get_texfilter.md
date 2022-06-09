# gpu_get_texfilter

With this function you can check to see whether texture filtering
(linear interpolation) is enabled (returns true ) or not (returns false
). For more information on texture filtering, see the function [
gpu_set_texfilter() ](gpu_set_texfilter) . **NOTE** : On the HTML5
target, this function will only work with WebGL enabled.

#### Syntax:

``` gml
gpu_get_texfilter();
```

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
if gpu_get_texfilter()
{
    gpu_set_texfilter(false);
}
else
{
    gpu_set_texfilter(true);
}
```

The above code checks to see if texture filtering is on or off and
switches it accordingly.

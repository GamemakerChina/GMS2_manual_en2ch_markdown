# gpu_get_tex_min_mip

With this function you can get the minimum mipmap level which is
currently used, where a value of 0 is the highest resolution, 1 is to
use the first mipmap, 2 is the second etc...

#### Syntax:

``` gml
gpu_get_tex_min_mip();
```

#### Returns:

``` gml
 Real

(default: 0)
```

#### Example:

``` gml
if gpu_get_tex_min_mip() != 0
{
    gpu_set_tex_min_mip(0);
}
```

The above code will check the current minimum mipmap level and if it is
not 0 it is set to 0.

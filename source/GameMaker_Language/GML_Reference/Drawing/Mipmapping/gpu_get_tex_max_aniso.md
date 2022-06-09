# gpu_get_tex_max_aniso

With this function you can get the current maximum level of anisotropy
when using the tf_anisotropic filter mode (see [
gpu_get_tex_mip_filter() ](gpu_get_tex_mip_filter) for more
information). The returned value will range between 1 and 16.

#### Syntax:

``` gml
gpu_get_tex_max_aniso();
```

#### Returns:

``` gml
 Real

(default: 16)
```

#### Example:

``` gml
if gpu_get_tex_max_aniso() != 8
{
    gpu_set_tex_max_aniso(8);
}
```

The above code will check the current maximum anisotropic filtering
level and if it is not 8 it is set to 8.

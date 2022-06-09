# gpu_set_tex_max_aniso

With this function you can set the current maximum level of anisotropy
when using the tf_anisotropic filter mode (see [
gpu_get_tex_mip_filter() ](gpu_get_tex_mip_filter) for more
information). The input value must range between 1 and 16.

#### Syntax:

``` gml
gpu_set_tex_max_aniso(maxaniso);
```

|          |                                                                         |                                                           |
|----------|-------------------------------------------------------------------------|-----------------------------------------------------------|
| Argument | Type                                                                    | Description                                               |
| maxaniso |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The maximum level for anisotropic filtering (default: 16) |

#### Returns:

``` gml
N/A
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

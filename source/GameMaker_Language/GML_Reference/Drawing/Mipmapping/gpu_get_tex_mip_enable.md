# gpu_get_tex_mip_enable

With this function you can get whether mipmapping is switched off,
switched on for everything or switched on only for texture groups
selected in the [Texture Group
Manager](../../../../Settings/Texture_Groups) . The function will
return one of the constants listed below, with the default setting being
mip_markedonly .

#### Syntax:

``` gml
gpu_get_tex_mip_enable();
```

#### Returns:

``` gml
 Constant
```

|                                                                                                                        |                                                                                                 |
|------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
|  [Mipmapping Constant](../../../../../GameMaker_Language/GML_Reference/Drawing/Mipmapping/gpu_get_tex_mip_enable)  |                                                                                                 |
| Constant                                                                                                               | Description                                                                                     |
|  mip_off                                                                                                               | Mipmapping is disabled.                                                                         |
|  mip_on                                                                                                                | Mipmapping for all textures is enabled.                                                         |
|  mip_markedonly                                                                                                        | Mipmapping is enabled for textures that have it enabled in the Texture Group options (default). |

#### Example:

``` gml
if gpu_get_tex_mip_enable != mip_on
{
    gpu_set_tex_mip_enable(mip_on);
}
```

The above code will check to see if mipmapping is enabled and if it is
not, it will enable it.

# gpu_set_tex_mip_enable

With this function you can change whether mipmapping is switched off,
switched on for everything, or switched on only for texture groups
selected in the [Texture Group
Manager](../../../../Settings/Texture_Groups) . The function
requires one of the constants listed below.

|                  |                                                                                                 |
|------------------|-------------------------------------------------------------------------------------------------|
| Constant         | Description                                                                                     |
|  mip_off         | Mipmapping is disabled.                                                                         |
|  mip_on          | Mipmapping for all textures is enabled.                                                         |
|  mip_markedonly  | Mipmapping is enabled for textures that have it enabled in the Texture Group options (default). |

#### Syntax:

``` gml
gpu_set_tex_mip_enable(setting);
```

|          |                                                                                                                        |                                                             |
|----------|------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| Argument | Type                                                                                                                   | Description                                                 |
| setting  |  [Mipmapping Constant](../../../../../GameMaker_Language/GML_Reference/Drawing/Mipmapping/gpu_get_tex_mip_enable)  | The mipmap setting (a constant, default: mip_markedonly )   |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if gpu_get_tex_mip_enable != mip_on
{
    gpu_set_tex_mip_enable(mip_on);
}
```

The above code will check to see if mipmapping is enabled and if it is
not, it will enable it.

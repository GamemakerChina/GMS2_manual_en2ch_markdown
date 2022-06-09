# gpu_set_tex_max_mip

With this function you can set the currently set maximum mipmap level
which is to be used, where a value of 0 is the highest resolution, 1 is
to use the first mipmap, 2 is the second etc... Note that this can be
quite useful for avoiding bleeding artifacts when rendering textures,
for example, setting the texture page border to 8px and then setting the
max mipmap level to 3 will ensure you don't get any bleeding problems at
greater render distances.

#### Syntax:

``` gml
gpu_set_tex_max_mip(maxmip);
```

|          |                                                                         |                                        |
|----------|-------------------------------------------------------------------------|----------------------------------------|
| Argument | Type                                                                    | Description                            |
| maxmip   |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The maximum mipmap level (default: 16) |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if gpu_get_tex_max_mip() != 4
{
    gpu_set_tex_max_mip(4);
}
```

The above code will check the current maximum mipmap level and if it is
not 4 it is set to 4.

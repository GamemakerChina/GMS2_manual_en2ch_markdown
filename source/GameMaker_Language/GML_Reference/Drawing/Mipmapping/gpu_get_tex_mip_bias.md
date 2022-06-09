# gpu_get_tex_mip_bias

With this function you can retrieve the mipmap bias value, where a value
of 0 equals no bias, 1 equals the first mipmap, 2 equals the second
mipmap etc... This controls the rate at which the mip map is swapped and
will generally make rendered textures blurrier the higher the value and
the greater the "distance" being viewed. Note that this can return
negative values too, in which case rendered textures will be sharper
over a greater distance the lower the value.

#### Syntax:

``` gml
gpu_get_tex_mip_bias();
```

#### Returns:

``` gml
 Real

(default: 0)
```

#### Example:

``` gml
if gpu_get_tex_mip_bias() != 0
{
    gpu_set_tex_mip_bias(0);
}
```

The above code will check the current mipmap bias and if it is not 0 it
is set to 0.

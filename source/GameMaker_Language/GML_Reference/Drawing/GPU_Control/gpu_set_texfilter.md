# gpu_set_texfilter

This function can be used to set the texture filtering (linear
interpolation) of all images drawn on the game screen. When this is
enabled ( true ) all textures will be smoothed when drawn (this includes
sprites as they too are considered textures), meaning that when scaled
or moved if there is not a 1:1 pixel ratio then there will be a
"smudging" across various pixels which may make images appear blurry
depending on the art style used. If this is disabled ( false ) then
images will be drawn based on the nearest pixel when scaled or moving
which may lead to "blocky" images. The default value is false , and this
can also be changed in the **Global Game Options** for individual target
platforms. **NOTE** :This setting will override any texture stage
interpolation set for shaders using the function [
gpu_set_texfilter_ext() ](gpu_set_texfilter_ext) . **NOTE** : On the
HTML5 target, this function will only work with WebGL enabled.

#### Syntax:

``` gml
gpu_set_texfilter(enable);
```

|          |                                                                            |                                                          |
|----------|----------------------------------------------------------------------------|----------------------------------------------------------|
| Argument | Type                                                                       | Description                                              |
| enable   |  [Boolean](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | Enable or disable texture filtering ( true / false )     |

#### Returns:

``` gml
N/A
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

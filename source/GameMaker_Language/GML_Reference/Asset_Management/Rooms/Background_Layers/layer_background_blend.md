# layer_background_blend

This function controls the blending (or "tinting") of the background
sprite and the default value is -1 (which represents the constant
c_white , which can also be used). Any other value (including internal
colour constants like c_red , or c_aqua ) will blend the specified
colour with the original sprite. You give the background element ID
(which you get when you create a background element using [
layer_background_create() ](layer_background_create) or when you use
the function [ layer_background_get_id() ](layer_background_get_id)
), and then set the blending colour to use. Below you can see an example
of a sprite that has been blended with different colours:  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/GML/Reference/Rooms/blend_image.png)  
Please note that you should try to limit blending on the **HTML5**
platform (unless using WebGL), as each blended sprite has to be cached
separately and so having many blended sprites may adversely affect
performance (you can also set the cache size using the function [
sprite_set_cache_size()
](../../Sprites/Sprite_Manipulation/sprite_set_cache_size) ).

#### Syntax:

``` gml
layer_background_blend(background_element_id, blend);
```

|                       |                                                                                                                                                    |                                                                        |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| Argument              | Type                                                                                                                                               | Description                                                            |
| background_element_id |  [Background Element ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/Background_Layers/layer_background_get_id)  | The unique ID value of the background element to change                |
| blend                 |  [Colour](../../../../../../GameMaker_Language/GML_Reference/Drawing/Colour_And_Alpha/Colour_And_Alpha)                                        | The colour to blend with the background sprite (default is c_white )   |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
var lay_id = layer_get_id("Background_sky"); var back_id = layer_background_get_id(lay_id); layer_background_blend(back_id, c_aqua);
```

The above code gets the ID value of the background assigned to the layer
"Background_sky" and then tints it to a colour.

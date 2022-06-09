# layer_sprite_blend

This function controls the blending (or "tinting") of the sprite sprite
and the default value is -1 (which represents the constant c_white ,
which can also be used). Any other value (including internal colour
constants like c_red , or c_aqua ) will blend the specified colour with
the original sprite. You give the sprite element ID (which you get when
you create a sprite element using [ layer_sprite_create()
](layer_sprite_create) or when you use the function [
layer_sprite_get_id() ](layer_sprite_get_id) ), and then set the
blending colour to use. Below you can see an example of a sprite that
has been blended with different colours:  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/GML/Reference/Rooms/blend_image.png)  
Please note that you should try to limit blending on the **HTML5**
platform (unless using WebGL), as each blended sprite has to be cached
separately and so having many blended sprites may adversely affect
performance (you can also set the cache size using the function [
sprite_set_cache_size()
](../../Sprites/Sprite_Manipulation/sprite_set_cache_size) ).

#### Syntax:

``` gml
layer_sprite_blend(sprite_element_id, blend);
```

|                   |                                                                                                                                        |                                                                    |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| Argument          | Type                                                                                                                                   | Description                                                        |
| sprite_element_id |  [Sprite Element ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/Sprite_Layers/layer_sprite_get_id)  | The unique ID value of the sprite element to change                |
| blend             |  [Colour](../../../../../../GameMaker_Language/GML_Reference/Drawing/Colour_And_Alpha/Colour_And_Alpha)                            | The colour to blend with the sprite sprite (default is c_white )   |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
var lay_id = layer_get_id("Asset_sky"); var spr_id = layer_sprite_get_id(lay_id, "Clouds"); layer_sprite_blend(spr_id, c_gray);
```

The above code gets the ID value of the sprite called "Clouds" assigned
to the layer "Asset_sky" and then tints it to a colour.

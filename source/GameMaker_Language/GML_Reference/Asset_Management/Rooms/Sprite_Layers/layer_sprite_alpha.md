# layer_sprite_alpha

This function controls the alpha (transparency) of the sprite on the
asset layer. You give the sprite element ID (which you get when you
create a sprite element using [ layer_sprite_create()
](layer_sprite_create) or when you use the function [
layer_sprite_get_id() ](layer_sprite_get_id) ), and then set the
alpha value to use. Alpha can be between 0 (fully transparent) and 1
(fully opaque) with the default alpha value for the sprite element
being 1. Note that if the layer the sprite element has been assigned to
is not visible - or the element itself has been made invisible - you
will not see any difference with this function until the layer or
element has been made visible again.

#### Syntax:

``` gml
layer_sprite_alpha(sprite_element_id, alpha);
```

|                   |                                                                                                                                        |                                                         |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| Argument          | Type                                                                                                                                   | Description                                             |
| sprite_element_id |  [Sprite Element ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/Sprite_Layers/layer_sprite_get_id)  | The unique ID value of the sprite element to change     |
| alpha             |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                              | The alpha for sprite sprite, from 0 to 1 (default is 1) |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
var lay_id = layer_get_id("Asset_sky"); var spr_id = layer_sprite_get_id(lay_id, "Clouds"); layer_sprite_alpha(spr_id, random(1));
```

The above code gets the ID value of the sprite asset named "Clouds"
assigned to the layer "Asset_sky" and then sets its alpha to a random
value between 0 and 1.

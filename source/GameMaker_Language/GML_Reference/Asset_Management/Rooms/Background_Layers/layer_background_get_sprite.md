# layer_background_get_sprite

This function can be used to get the current sprite index value of the
background element. You give the background element ID (which you get
when you create a background element using [ layer_background_create()
](layer_background_create) or when you use the function [
layer_background_get_id() ](layer_background_get_id) ), and the
function will return a real value that represents the sprite index being
shown. If the element has no sprite assigned, the function will return
-1.

#### Syntax:

``` gml
layer_background_get_sprite(background_element_id);
```

|                       |                                                                                                                                                    |                                                                           |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| Argument              | Type                                                                                                                                               | Description                                                               |
| background_element_id |  [Background Element ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/Background_Layers/layer_background_get_id)  | The unique ID value of the background element to get the information from |

#### Returns:

``` gml
 Sprite Asset

or -1
```

#### Example:

``` gml
var lay_id = layer_get_id("Background_sky");
var back_id = layer_background_get_id(lay_id);
if layer_background_get_sprite(back_id) != spr_Clouds
{
    layer_background_sprite(back_id, spr_Clouds);
}
```

The above code will get the layer ID for the layer named
"Background_sky" and then use that to get the ID of the background
element on that layer. This ID is then used to check the sprite assigned
to the element, setting it to the sprite "spr_Clouds" if it is not
already.

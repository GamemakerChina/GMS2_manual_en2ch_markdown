# layer_background_get_blend

This function can be used to get the blend colour of the background
element. You give the background element ID (which you get when you
create a background element using [ layer_background_create()
](layer_background_create) or when you use the function [
layer_background_get_id() ](layer_background_get_id) ), and the
function will return real value that represents the colour assigned.

#### Syntax:

``` gml
layer_background_get_blend(background_element_id);
```

|                       |                                                                                                                                                    |                                                                           |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| Argument              | Type                                                                                                                                               | Description                                                               |
| background_element_id |  [Background Element ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/Background_Layers/layer_background_get_id)  | The unique ID value of the background element to get the information from |

#### Returns:

``` gml
 Colour
```

#### Example:

``` gml
var lay_id = layer_get_id("Background_sky");
var back_id = layer_background_get_id(lay_id);
if layer_background_get_blend(back_id) == c_white
{
    layer_background_blend(back_id, make_colour_rgb(random(255), random(255), 255));
}
```

The above code will get the layer ID for the layer named
"Background_sky" and then use that to get the ID of the background
element on that layer. This ID is then used to check the element blend
colour and if it is equivalent to the constant c_white , then the layer
blend is set to a random colour.

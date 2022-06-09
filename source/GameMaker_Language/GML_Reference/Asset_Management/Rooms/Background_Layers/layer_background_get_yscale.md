# layer_background_get_yscale

This function can be used to get the current scale multiplier value of
the background element. You give the background element ID (which you
get when you create a background element using [
layer_background_create() ](layer_background_create) or when you use
the function [ layer_background_get_id() ](layer_background_get_id)
), and the function will return real value that represents the scale
multiplier being used to draw the sprite. Default value is 1.

#### Syntax:

``` gml
layer_background_get_yscale(background_element_id);
```

|                       |                                                                                                                                                    |                                                                           |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| Argument              | Type                                                                                                                                               | Description                                                               |
| background_element_id |  [Background Element ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/Background_Layers/layer_background_get_id)  | The unique ID value of the background element to get the information from |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
var lay_id = layer_get_id("Background_sky");
var back_id = layer_background_get_id(lay_id);
if layer_background_get_yscale(back_id) != -1
{
    layer_background_yscale(back_id, -1);
}
```

The above code will get the layer ID for the layer named
"Background_sky" and then use that to get the ID of the background
element on that layer. This ID is then used to check the y scale for the
element and if it is not -1, it is set to -1.

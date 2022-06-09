# layer_background_get_htiled

This function can be used to find out if the background element is tiled
horizontally or not. You give the background element ID (which you get
when you create a background element using [ layer_background_create()
](layer_background_create) or when you use the function [
layer_background_get_id() ](layer_background_get_id) ), and the
function will return either true if the element is currently tiled, or
false if it is not.

#### Syntax:

``` gml
layer_background_get_htiled(background_element_id);
```

|                       |                                                                                                                                                    |                                                                           |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| Argument              | Type                                                                                                                                               | Description                                                               |
| background_element_id |  [Background Element ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/Background_Layers/layer_background_get_id)  | The unique ID value of the background element to get the information from |

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
var lay_id = layer_get_id("Background_sky");
var back_id = layer_background_get_id(lay_id);
if !layer_background_get_htiled(back_id)
{
    layer_background_htiled(back_id, true);
}
```

The above code will get the layer ID for the layer named
"Background_sky" and then use that to get the ID of the background
element on that layer. This ID is then used to check if the element is
tiling across the horizontal axis, and if it is not then it is set to do
so.

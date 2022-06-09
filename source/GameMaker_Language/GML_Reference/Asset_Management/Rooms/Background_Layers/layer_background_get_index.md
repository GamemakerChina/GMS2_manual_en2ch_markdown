# layer_background_get_index

This function can be used to get the current image index value of the
background element. You give the background element ID (which you get
when you create a background element using [ layer_background_create()
](layer_background_create) or when you use the function [
layer_background_get_id() ](layer_background_get_id) ), and the
function will return real value that represents the image index being
shown for the sprite. The function will return -1 if either the
background element doesn't exist or the element doesn't have a valid
sprite assigned to it.

#### Syntax:

``` gml
layer_background_get_index(background_element_id);
```

|                       |                                                                                                                                                    |                                                                           |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| Argument              | Type                                                                                                                                               | Description                                                               |
| background_element_id |  [Background Element ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/Background_Layers/layer_background_get_id)  | The unique ID value of the background element to get the information from |

#### Returns:

``` gml
 Real

(the current sprite image index or -1)
```

#### Example:

``` gml
var lay_id = layer_get_id("Background_sky");
var back_id = layer_background_get_id(lay_id);
if layer_background_get_index(back_id) &amp;lt; 4
{
    layer_background_index(back_id, 4);
}
```

The above code will get the layer ID for the layer named
"Background_sky" and then use that to get the ID of the background
element on that layer. This ID is then used to check if the image index
for the element is less than 4, and if so it is set to 4.

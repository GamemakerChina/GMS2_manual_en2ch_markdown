# layer_background_get_stretch

This function can be used to get the stretched state of the background
element sprite. You give the background element ID (which you get when
you create a background element using [ layer_background_create()
](layer_background_create) or when you use the function [
layer_background_get_id() ](layer_background_get_id) ), and the
function will return either true if the element sprite is currently
stretched to fit the room, or false if it is not.

#### Syntax:

``` gml
layer_background_get_stretch(background_element_id);
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
if layer_background_get_stretch(back_id)
{
    layer_background_stretch(back_id, false);
}
```

The above code will get the layer ID for the layer named
"Background_sky" and then use that to get the ID of the background
element on that layer. This ID is then used to check and see if the
element sprite will be stretched to fit the room or not and if it is
stretched, then this property is set to false .

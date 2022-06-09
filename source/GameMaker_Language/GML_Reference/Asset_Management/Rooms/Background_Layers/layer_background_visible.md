# layer_background_visible

Using this function you can toggle a background elements visibility. You
supply the background element ID (which you get when you create a
background element using [ layer_background_create()
](layer_background_create) or when you use the function [
layer_background_get_id() ](layer_background_get_id) ), and then set
the visible argument to true or false . When set to true the element
will be displayed, and when set to false , the element will not be
displayed. Note that this is dependent on the layer visibility, and even
if the background element is flagged as visible, it will not be drawn if
the layer it is on is flagged as not visible.

#### Syntax:

``` gml
layer_background_visible(background_element_id, visible)
```

|                       |                                                                                                                                                    |                                                         |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| Argument              | Type                                                                                                                                               | Description                                             |
| background_element_id |  [Background Element ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/Background_Layers/layer_background_get_id)  | The unique ID value of the background element to change |
| visible               |  [Boolean](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                       | The visibility toggle, which can be true or false       |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if mouse_check_button_pressed(mb_left)
{
    var back = layer_background_get_id(layer);
    if layer_background_get_visible(back)
    {
        layer_background_visible(back, false);
    }
    else
    {
        layer_background_visible(back, true);
    }
}
```

The above code checks for a mouse button press and if one is detected it
will toggle the background visibility of the background element assigned
to the layer the instance running the code is on.

# layer_background_stretch

Using this function you can toggle a background element sprite to
stretch to fit the room or remain at 1:1 with the resolution. You supply
the background element ID (which you get when you create a background
element using [ layer_background_create() ](layer_background_create)
or when you use the function [ layer_background_get_id()
](layer_background_get_id) ), and then set the stretch argument to
true or false . When set to true the element sprite will be stretched to
fit the room (either scaled up or scaled down depending on the sizes of
the sprite and the room), and when set to false , the element sprite
will be displayed at its native resolution.

#### Syntax:

``` gml
layer_background_stretch(background_element_id, stretch)
```

|                       |                                                                                                                                                    |                                                         |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| Argument              | Type                                                                                                                                               | Description                                             |
| background_element_id |  [Background Element ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/Background_Layers/layer_background_get_id)  | The unique ID value of the background element to change |
| stretch               |  [Boolean](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                       | The stretch toggle, which can be true or false          |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if mouse_check_button_pressed(mb_left)
{
    var back = layer_background_get_id(layer);
    if layer_background_get_stretch(back)
    {
        layer_background_stretch(back, false);
    }
    else
    {
        layer_background_stretch(back, true);
    }
}
```

The above code checks for a mouse button press and if one is detected it
will toggle the stretching of the background element sprite assigned to
the layer the instance running the code is on.

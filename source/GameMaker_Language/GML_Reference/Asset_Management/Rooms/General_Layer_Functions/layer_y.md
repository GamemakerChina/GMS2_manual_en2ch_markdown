# layer_y

You can use this function to set the y position of the layer within the
currently scoped room. You supply the layer ID (which you get when you
create the layer using [ layer_create() ](layer_create) ) or the
layer name (as a string - this will have a performance impact) and the
function will move the layer the given number of pixels along the
vertical axis of the room.

#### Syntax:

``` gml
layer_y(layer_id, y)
```

|          |                                                                                                                                                                                                                  |                                                           |
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| Argument | Type                                                                                                                                                                                                             | Description                                               |
| layer_id |  [String](../../../../../../GameMaker_Language/GML_Overview/Data_Types) or [Layer ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/General_Layer_Functions/layer_get_id)    | The unique ID value of the layer to set the y position of |
| y        |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                                                                                        | The y position in the room to set the layer to            |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
var lay_id = layer_get_id("Sprites");
if layer_get_x(lay_id) != 0 || layer_get_y(lay_id) != 0
{
    layer_x(lay_id, 0);
    layer_y(lay_id, 0);
}
```

The above code checks the given layer position and if it is not set to
(0, 0) then it is set to that position.

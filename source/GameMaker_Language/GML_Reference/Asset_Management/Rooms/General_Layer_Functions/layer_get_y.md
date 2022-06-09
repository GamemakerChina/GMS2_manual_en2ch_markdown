# layer_get_y

You can use this function to retrieve the y position of the layer within
the currently scoped room. You supply the layer ID (which you get when
you create the layer using [ layer_create() ](layer_create) ) or the
layer name (as a string - this will have a performance impact) and the
function returns a real number for the x position of the layer, relative
to the (0,0) position of the room. Default is 0.

#### Syntax:

``` gml
layer_get_y(layer_id)
```

|          |                                                                                                                                                                                                                  |                                                           |
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| Argument | Type                                                                                                                                                                                                             | Description                                               |
| layer_id |  [String](../../../../../../GameMaker_Language/GML_Overview/Data_Types) or [Layer ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/General_Layer_Functions/layer_get_id)    | The unique ID value of the layer to get the y position of |

#### Returns:

``` gml
 Real
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

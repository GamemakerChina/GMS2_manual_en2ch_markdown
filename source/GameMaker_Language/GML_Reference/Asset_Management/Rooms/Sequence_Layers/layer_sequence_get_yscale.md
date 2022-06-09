# layer_sequence_get_yscale

With this function you supply the sequence element ID - as returned by [
layer_sequence_create() ](layer_sequence_create) or by one of the
[layer element
functions](../General_Layer_Functions/General_Layer_Functions) - and
it will return the current scale along the Y axis of the sequence
element in the game room.

#### Syntax:

``` gml
layer_sequence_get_yscale(sequence_element_id)
```

|                     |                                                                                                                                              |                                                       |
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| Argument            | Type                                                                                                                                         | Description                                           |
| sequence_element_id |  [Sequence Element ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/Sequence_Layers/layer_sequence_create)  | The unique ID value of the sequence element to target |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
var _ys = layer_sequence_get_yscale(title_sequence)
if _ys &amp;lt; 1
{
    _ys += 0.01;
    layer_sequence_yscale(title_sequence, _ys);
}
```

The above code retrieves the current scale along the Y axis of the the
sequence element with the ID stored in the variable "title_sequence",
and if it's less than 1, then 0.01 is added to the current Y scale.

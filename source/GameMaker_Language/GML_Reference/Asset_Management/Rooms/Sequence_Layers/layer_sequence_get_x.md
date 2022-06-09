# layer_sequence_get_x

With this function you supply the sequence element ID - as returned by [
layer_sequence_create() ](layer_sequence_create) or by one of the
[layer element
functions](../General_Layer_Functions/General_Layer_Functions) - and
it will return the current X position in the game room for the sequence.

#### Syntax:

``` gml
layer_sequence_get_x(sequence_element_id)
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
if layer_sequence_get_x(title_sequence) != room_width / 2
{
    layer_sequence_x(title_sequence, room_width / 2);
}
```

The above code checks the X position of the sequence element ID stored
in the variable "title_sequence", and if it's not set to half the room
width, it is set to this value.

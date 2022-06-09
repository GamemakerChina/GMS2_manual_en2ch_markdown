# layer_sequence_x

With this function you can set the position along the X (horizontal)
axis of the room for the given sequence element. You supply the sequence
element ID as returned by [ layer_sequence_create()
](layer_sequence_create) or by one of the [layer element
functions](../General_Layer_Functions/General_Layer_Functions) along
with the X position to set and the sequence will be moved to the new
position.

#### Syntax:

``` gml
layer_sequence_x(sequence_element_id, pos_x)
```

|                     |                                                                                                                                              |                                                       |
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| Argument            | Type                                                                                                                                         | Description                                           |
| sequence_element_id |  [Sequence Element ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/Sequence_Layers/layer_sequence_create)  | The unique ID value of the sequence element to target |
| pos_x               |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                    | The X position to move the sequence element to        |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if layer_sequence_exists(my_seq)
{
    layer_sequence_x(my_seq, x);
    layer_sequence_y(my_seq, y);
}
```

The above code checks to see if the sequence element referenced in the
variable "my_seq" exists, and if it does it sets the x/y position to the
that of the instance running the code.

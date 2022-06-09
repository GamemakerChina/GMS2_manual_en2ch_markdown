# layer_sequence_get_headdir

With this function you supply the sequence element ID - as returned by [
layer_sequence_create() ](layer_sequence_create) or by one of the
[layer element
functions](../General_Layer_Functions/General_Layer_Functions) - and
it will return the current playhead direction, which will be one of the
constants listed below.

#### Syntax:

``` gml
layer_sequence_get_headdir(sequence_element_id)
```

|                     |                                                                                                                                              |                                                       |
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| Argument            | Type                                                                                                                                         | Description                                           |
| sequence_element_id |  [Sequence Element ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/Sequence_Layers/layer_sequence_create)  | The unique ID value of the sequence element to target |

#### Returns:

``` gml
 Constant
```

|               |                                                                           |       |
|---------------|---------------------------------------------------------------------------|-------|
| Constant      | Description                                                               | Value |
| seq_dir_right | The sequence is playing frames in an incremental order from left to right | 1     |
| seq_dir_left  | The sequence is playing frames in a decremental order from right to left  | -1    |

#### Example:

``` gml
if layer_sequence_get_headdir(title_sequence) != seq_dir_left
{
    layer_sequence_headdir(title_sequence, seq_dir_left);
}
```

The above code checks the the current playhead direction of the sequence
element ID stored in the variable "title_sequence", and if it's not set
to seq_dir_left , it is set to this value.

# layer_sequence_get_headpos

With this function you supply the sequence element ID - as returned by [
layer_sequence_create() ](layer_sequence_create) or by one of the
[layer element
functions](../General_Layer_Functions/General_Layer_Functions) - and
it will return the current playhead position (the current frame the
playhead is on).

#### Syntax:

``` gml
layer_sequence_get_headpos(sequence_element_id)
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
if layer_sequence_get_headpos(title_sequence) != 0
{
    layer_sequence_headpos(title_sequence, 0);
}
```

The above code checks the current playhead position of the sequence
element ID stored in the variable "title_sequence", and if it's not set
to 0, it is set to this value.

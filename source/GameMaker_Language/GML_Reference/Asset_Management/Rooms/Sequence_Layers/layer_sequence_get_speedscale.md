# layer_sequence_get_speedscale

With this function you supply the sequence element ID - as returned by [
layer_sequence_create() ](layer_sequence_create) or by one of the
[layer element
functions](../General_Layer_Functions/General_Layer_Functions) - and
it will return the current playback speed scale. This is the
*multiplier* value used to slow down or speed up the playback speed. A
value of 1 is the default value, and values lower than 1 mean that
playback is slowed down and values greater than 1 mean that playback is
sped up.

#### Syntax:

``` gml
layer_sequence_get_speedscale(sequence_element_id)
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
if layer_sequence_get_speedscale(title_sequence) != 1
{
    layer_sequence_speedscale(title_sequence, 1);
}
```

The above code checks the the current playhead speed scale of the
sequence element ID stored in the variable "title_sequence", and if it's
not set to 1 it is set to this value.

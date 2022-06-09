# layer_sequence_get_length

With this function you supply the sequence element ID - as returned by [
layer_sequence_create() ](layer_sequence_create) or by one of the
[layer element
functions](../General_Layer_Functions/General_Layer_Functions) - and
it will return the length of the sequence. This is the number of frames
that the sequence will run for.

#### Syntax:

``` gml
layer_sequence_get_length(sequence_element_id)
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
var _frames = layer_sequence_get_length(my_seq); alarm[0] = frames;
```

The above code retrieves the number of frames that a sequence will run
then uses this value to set an alarm.

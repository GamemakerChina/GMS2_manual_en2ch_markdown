# layer_sequence_get_sequence

With this function you supply the sequence element ID - as returned by [
layer_sequence_create() ](layer_sequence_create) or by one of the
[layer element
functions](../General_Layer_Functions/General_Layer_Functions) - and
it will return the sequence object
[struct](../../../../GML_Overview/Structs) . This function bypasses
the need to first get the sequence instance struct and permits you to
access the sequence data directly. You can find out more about the
format of the sequence object struct on [this
page](../../Sequences/Sequence_Structs/The_Sequence_Object_Struct) .

#### Syntax:

``` gml
layer_sequence_get_sequence(sequence_element_id)
```

|                     |                                                                                                                                              |                                                       |
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| Argument            | Type                                                                                                                                         | Description                                           |
| sequence_element_id |  [Sequence Element ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/Sequence_Layers/layer_sequence_create)  | The unique ID value of the sequence element to target |

#### Returns:

``` gml
 Sequence Object Struct
```

#### Example:

``` gml
var _seq = layer_sequence_create("Background", 0, 0, seq_AnimatedBackground);
var _struct = layer_sequence_get_sequence(_seq);
_struct.playbackSpeedType = spritespeed_framespersecond;
_struct.playbackSpeed = 30;
```

The above code creates a new sequence element and then retrieves its
sequence data struct. This is then used to change the playback speed and
type of the sequence.

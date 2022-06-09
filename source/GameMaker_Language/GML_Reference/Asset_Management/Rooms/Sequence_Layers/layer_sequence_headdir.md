# layer_sequence_headdir

With this function you can set the direction for the given sequence
playhead . You supply the sequence element ID as returned by [
layer_sequence_create() ](layer_sequence_create) or by one of the
[layer element
functions](../General_Layer_Functions/General_Layer_Functions) , and
then give the playhead direction which should be one of the following
constants:

|                 |                                                                          |       |
|-----------------|--------------------------------------------------------------------------|-------|
| Constant        | Description                                                              | Value |
|  seq_dir_right  | The sequence will play frames in an incremental order from left to right | 1     |
|  seq_dir_left   | The sequence will play frames in a decremental order from right to left  | -1    |

#### Syntax:

``` gml
layer_sequence_headdir(sequence_element_id, direction)
```

|                     |                                                                                                                                                                  |                                                       |
|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| Argument            | Type                                                                                                                                                             | Description                                           |
| sequence_element_id |  [Sequence Element ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/Sequence_Layers/layer_sequence_create)                      | The unique ID value of the sequence element to target |
| direction           |  [Sequence Direction Constant](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Sequences/Sequence_Structs/The_Sequence_Instance_Struct)  | The playhead direction, a constant, listed above      |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
var _seq = layer_sequence_create("Background", 0, 0, seq_AnimatedBackground);
layer_sequence_headdir(_seq, seq_dir_left);
```

The above code creates a new sequence and stores its ID in a local
variable. This ID is then used to set the playhead direction to
decrement frames (right to left playback).

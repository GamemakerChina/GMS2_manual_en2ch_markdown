# layer_sequence_get_instance

With this function you supply the sequence element ID - as returned by [
layer_sequence_create() ](layer_sequence_create) or by one of the
[layer element
functions](../General_Layer_Functions/General_Layer_Functions) - and
it will return the sequence *instance*
[struct](../../../../GML_Overview/Structs) . You can find out more
about the format of the sequence instance struct on [this
page](../../Sequences/Sequence_Structs/The_Sequence_Instance_Struct)
.

#### Syntax:

``` gml
layer_sequence_get_instance(sequence_element_id)
```

|                     |                                                                                                                                              |                                                       |
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| Argument            | Type                                                                                                                                         | Description                                           |
| sequence_element_id |  [Sequence Element ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/Sequence_Layers/layer_sequence_create)  | The unique ID value of the sequence element to target |

#### Returns:

``` gml
 Sequence Instance Struct
```

#### Example:

``` gml
var _seq = layer_sequence_create("Background", 0, 0, seq_AnimatedBackground);
var _struct = layer_sequence_get_instance(_seq);
_struct.speedScale = 0.5;
```

The above code creates a new sequence element and then retrieves its
sequence instance ID. This is then used to change the playback speed
scale property of the sequence instance.

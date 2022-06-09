# layer_sequence_create

With this function you can create an instance of a sequence asset on the
given layer. You supply the layer ID which can be a string of the layer
name - as defined in the room editor - or the unique layer ID - as
returned by the function [ layer_get_id()
](../General_Layer_Functions/layer_get_id) , as well as the X and Y
position in the room to create the sequence at, and finally the ID of
the sequence to create. The sequence ID is the name constant that you
defined in the Asset Browser for the sequence. The function will return
the unique ID of the sequence element, which can then be used in all
further layer functions for sequences, or it can be used to retrieve the
sequence instance struct using the function [
layer_sequence_get_instance() ](layer_sequence_get_sequence) . It is
worth noting that if the sequence contains any object tracks, their
instances will be created as soon as the sequence element itself is
created, regardless of where their asset keys are positioned on the
[Dope
Sheet](../../../../../The_Asset_Editors/Sequence_Properties/Using_The_Dope_Sheet)
. The Sequence controller simply toggles the
[visibility](../../Instances/Instance_Variables/visible) of the
instance to hide and show it depending on the position and duration of
the track's asset key and does *not* repeatedly create and destroy it.
As a result, instances will run their Create events when the sequence
element is created and not when their asset keys begin.

#### Syntax:

``` gml
layer_sequence_create(layer_id, x, y, sequence_id)
```

|             |                                                                                                                                                                                                                  |                                                            |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| Argument    | Type                                                                                                                                                                                                             | Description                                                |
| layer_id    |  [String](../../../../../../GameMaker_Language/GML_Overview/Data_Types) or [Layer ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/General_Layer_Functions/layer_get_id)    | The unique ID value of the instance layer to target        |
| x           |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                                                                                        | The x position in the room to create the sequence at       |
| y           |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                                                                                        | The y position in the room to create the sequence at       |
| sequence_id |  [Sequence Asset](../../../../../../The_Asset_Editors/Sequences)                                                                                                                                             | The sequence asset to use, as defined in the Asset Browser |

#### Returns:

``` gml
 Sequence Element ID
```

#### Example:

``` gml
var _s = layer_sequence_create("Background", 0, 0, seq_AnimatedBackground);
layer_sequence_pause(_s);
```

The above code creates a new sequence on the layer "Background" then
pauses it.

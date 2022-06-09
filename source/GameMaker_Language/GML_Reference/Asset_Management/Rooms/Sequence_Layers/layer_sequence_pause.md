# layer_sequence_pause

With this function you can pause the playback of the given sequence. You
supply the sequence element ID as returned by [ layer_sequence_create()
](layer_sequence_create) or by one of the [layer element
functions](../General_Layer_Functions/General_Layer_Functions) and
the function will pause the sequence until you begin playback again
using the function [ layer_sequence_play() ](layer_sequence_play) .

#### Syntax:

``` gml
layer_sequence_pause(sequence_element_id)
```

|                     |                                                                                                                                              |                                                       |
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| Argument            | Type                                                                                                                                         | Description                                           |
| sequence_element_id |  [Sequence Element ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/Sequence_Layers/layer_sequence_create)  | The unique ID value of the sequence element to target |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
var _seq = layer_sequence_create("Background", 0, 0, seq_AnimatedBackground);
if global.Pause
{
    layer_sequence_pause(_seq);
}
```

The above code creates a new sequence and stores its ID in a local
variable. It then checks to see if the game is paused, and if it is it
pauses the playback of the sequence.

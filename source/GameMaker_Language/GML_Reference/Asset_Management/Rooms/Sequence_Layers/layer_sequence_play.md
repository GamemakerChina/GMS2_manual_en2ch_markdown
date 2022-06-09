# layer_sequence_play

With this function you can start the playback of the given sequence. You
supply the sequence element ID as returned by [ layer_sequence_create()
](layer_sequence_create) or by one of the [layer element
functions](../General_Layer_Functions/General_Layer_Functions) and
the function will play the sequence, which you can then pause if
required using the function [ layer_sequence_pause()
](layer_sequence_pause) . **IMPORTANT!** If your sequence has any
instances in it, these instances shouldn't change their image_xscale /
image_yscale / image_angle / x / y variables as they will be overwritten
when the sequence updates each step after starting to be played.

#### Syntax:

``` gml
layer_sequence_play(sequence_element_id)
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
if keyboard_check_pressed(ord("P"))
{
    global.Pause = !global.Pause;
    var a = layer_get_all_elements(layer);
    for (var i = 0; i &amp;lt; array_length(a); i++;)
    {
        if layer_get_element_type(a[i]) == layerelementtype_sequence
        {
            if global.Pause
            {
                layer_sequence_pause(a[i]);
            }
            else
            {
                layer_sequence_play(a[i]);
            }
        }
    }
}
```

The above code checks to see if the game has been paused or not when a
key is pressed. If the game is paused, then it loops through all
sequence elements on the current layer (the layer of the calling
instance) and pauses their playback, and if the game is not paused, then
the loop will start their playback again.

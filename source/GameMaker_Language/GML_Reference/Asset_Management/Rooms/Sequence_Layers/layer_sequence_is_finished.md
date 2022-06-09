# layer_sequence_is_finished

With this function you supply the sequence element ID - as returned by [
layer_sequence_create() ](layer_sequence_create) or by one of the
[layer element
functions](../General_Layer_Functions/General_Layer_Functions) - and
it will check if the sequence is finished playing or not, returning true
if it is, and false if it is not. Note that this is only applicable when
the sequence is *not* set to loop or ping-pong in the playback mode.

#### Syntax:

``` gml
layer_sequence_is_finished(sequence_element_id)
```

|                     |                                                                                                                                              |                                                       |
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| Argument            | Type                                                                                                                                         | Description                                           |
| sequence_element_id |  [Sequence Element ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/Sequence_Layers/layer_sequence_create)  | The unique ID value of the sequence element to target |

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
if layer_sequence_is_finished(title_sequence) != 0
{
    alarm[0] = room_speed * 3;
    layer_sequence_play(title_sequence);
}
```

The above code checks if the sequence element ID stored in the variable
"title_sequence" is finished, and if it is it starts it playing again
and sets an alarm.

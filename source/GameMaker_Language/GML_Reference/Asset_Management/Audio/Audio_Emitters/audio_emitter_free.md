# audio_emitter_free

With this function you can remove the given emitter from memory. This
should always be done whenever the emitter is not going to be used
further in the room or the game, ie: in the [Destroy
Event](../../../../../The_Asset_Editors/Object_Properties/Object_Events)
of the instance or in the [Room End
Event](../../../../../The_Asset_Editors/Object_Properties/Other_Events)
, otherwise you may end up with a memory leak that will slow down and
eventually crash your game.

#### Syntax:

``` gml
audio_emitter_free(emitter);
```

|          |                                                                                                                                         |                                   |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| Argument | Type                                                                                                                                    | Description                       |
| emitter  |  [Audio Emitter ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Audio/Audio_Emitters/audio_emitter_create)  | The index of the emitter to free. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if lives = 0
{
    audio_emitter_free(s_emit);
    room_goto(rm_Menu);
}
```

The above code checks the value of the global variable "lives" and if it
returns 0, it will destroy the emitter indexed in the variable "s_emit"
and then go to the room indexed in the variable "rm_Menu".

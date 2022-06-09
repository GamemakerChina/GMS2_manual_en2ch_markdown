# audio_emitter_get_listener_mask

This function will return the bit-mask data that defines which audio
listeners an emitter should play sounds from. For more information see
the section on [Audio Listeners](../Audio_Listeners/Audio_Listeners)
.

#### Syntax:

``` gml
audio_emitter_get_listener_mask(emitterID);
```

|           |                                                                                                                                         |                                                 |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| Argument  | Type                                                                                                                                    | Description                                     |
| emitterID |  [Audio Emitter ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Audio/Audio_Emitters/audio_emitter_create)  | The unique ID of the emitter to get the mask of |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
s_emit = audio_emitter_create();
if audio_emitter_get_listener_mask(s_emit) != global.PlayerMask
{
    audio_emitter_set_listener_mask(snd, global.PlayerMask);
}
```

The above code creates an emitter then checks the listener mask data for
it, and if it's not the same as that which is stored in a global
variable, it sets the listener(s) to play from using the mask data
stored in the global variable.

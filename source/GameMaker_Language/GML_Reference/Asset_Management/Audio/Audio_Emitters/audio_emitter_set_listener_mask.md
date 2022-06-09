# audio_emitter_set_listener_mask

This function can be used to set the the bit-mask for an emitter so that
all sounds played through the emitter will play only from those
listeners specified. You can create a bit-mask by using the [
audio_get_listener_info()
](../Audio_Listeners/audio_get_listener_info) and then using the
bitwise or ("\|") to create a custom mask with those listeners that you
require the sound to play from, and then apply this custom mask to the
emitter. This mask will over-ride the default mask or that which you may
have set using the function [ audio_set_listener_mask()
](../Audio_Listeners/audio_set_listener_mask) .

#### Syntax:

``` gml
audio_emitter_set_listener_mask(emitterID, mask);
```

|           |                                                                                                                                         |                                                 |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| Argument  | Type                                                                                                                                    | Description                                     |
| emitterID |  [Audio Emitter ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Audio/Audio_Emitters/audio_emitter_create)  | The unique ID of the emitter to set the mask of |
| mask      |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                               | The bitmask data to set for the sound           |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
s_emit = audio_emitter_create();
audio_emitter_set_listener_mask(snd, global.PlayerMask);
```

The above code creates an audio emitter and then sets the listener(s) to
play from using the mask data stored in a global variable.

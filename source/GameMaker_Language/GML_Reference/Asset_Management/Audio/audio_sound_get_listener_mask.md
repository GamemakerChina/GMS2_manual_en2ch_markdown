# audio_sound_get_listener_mask

This function will return the bit-mask data that defines which audio
listeners a sound should be played from. See the section on [Audio
Listeners](Audio_Listeners/Audio_Listeners) for more information.

#### Syntax:

``` gml
audio_sound_get_listener_mask(soundID);
```

|          |                                                                                                                    |                                               |
|----------|--------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| Argument | Type                                                                                                               | Description                                   |
| soundID  |  [Sound Instance ID](../../../../../GameMaker_Language/GML_Reference/Asset_Management/Audio/audio_play_sound)  | The unique ID of the sound to get the mask of |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
var snd = audio_play_sound(snd_PlayerDead, 10, false);
if audio_sound_get_listener_mask(snd) != global.PlayerMask
{
    audio_sound_set_listener_mask(snd, global.PlayerMask);
}
```

The above code plays a sound then checks the listener mask data for the
sound, and if it's not the same as that which is stored in a global
variable, it sets the listener(s) to play from using the mask data
stored in the global variable.

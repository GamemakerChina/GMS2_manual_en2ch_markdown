# audio_emitter_get_pitch

This function returns the current pitch value set for the given audio
emitter.

#### Syntax:

``` gml
audio_emitter_get_pitch(emitter);
```

|          |                                                                                                                                         |                                  |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| Argument | Type                                                                                                                                    | Description                      |
| emitter  |  [Audio Emitter ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Audio/Audio_Emitters/audio_emitter_create)  | The index of the emitter to use. |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
if audio_emitter_get_pitch(emitter_player) != 1
{
    audio_emitter_pitch(emitter_player, 1);
}
```

The above code checks the current pitch of a given emitter and if it is
not equal to 1 it is set to 1.

# audio_emitter_get_vy

This function returns the current velocity along the y axis for the
given audio emitter.

#### Syntax:

``` gml
audio_emitter_get_vy(emitter);
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
if audio_emitter_get_vy(emitter_player) != 0
{
    audio_emitter_velocity(emitter_player, 0, 0, 0);
}
```

The above code checks the current y velocity of a given emitter and if
it is not equal to 0, it is set to 0.

# audio_emitter_get_z

This function returns the current z position of the given audio emitter.

#### Syntax:

``` gml
audio_emitter_get_z(emitter);
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
if audio_emitter_get_z(emitter_player) != 0
{
    var ex = audio_emitter_get_x(emitter_player);
    var ey = audio_emitter_get_y(emitter_player);
    audio_emitter_position(emitter_player, ex, ey, 0);
}
```

The above code checks the current z position of a given emitter and if
it is not equal to 0, it is set to 0.

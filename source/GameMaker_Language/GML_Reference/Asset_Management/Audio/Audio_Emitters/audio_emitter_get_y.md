# audio_emitter_get_y

This function returns the current y position of the given audio emitter.

#### Syntax:

``` gml
audio_emitter_get_y(emitter);
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
if audio_emitter_get_y(emitter_player) != x
{
    audio_emitter_position(emitter_player, x, y, 0);
}
```

The above code checks the current y position of a given emitter and if
it is not equal to the instance y position, it is set to the instance
position.

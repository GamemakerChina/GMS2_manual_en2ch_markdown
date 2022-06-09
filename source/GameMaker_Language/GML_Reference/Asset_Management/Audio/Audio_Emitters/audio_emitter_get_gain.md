# audio_emitter_get_gain

This function returns the current gain (volume) set for the given audio
emitter, normally between 0 and 1, where 0 is silent and 1 is full
volume. Note that on some platforms you can have a gain of greater than
1, although a value of 1 is considered "full volume" and anything
greater may introduce audio clipping.

#### Syntax:

``` gml
audio_emitter_get_gain(emitter);
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
if audio_emitter_get_gain(emitter_player) &amp;lt; 1
{
    audio_emitter_gain(emitter_player, 1);
}
```

The above code checks the current gain of a given emitter and if it is
less than 1 it is set to 1.

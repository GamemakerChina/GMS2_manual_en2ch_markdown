# audio_sound_set_track_position

This function will set the position (in seconds) for the given sound ID
or asset. The supplied "index" can either be a single instance of a
sound (as returned from [ audio_play_sound() ](audio_play_sound) )
or a sound asset (e.g. one added via the Asset Browser). The behaviour
of this function will differ depending on the kind of index you have
specified:

-   If it's a unique sound ID that you use, which is already playing,
    then its position will immediately change to the given time.
-   If it's a sound asset, then all further plays of the given sound
    asset will start at the new time.

This function will only change the track position for the currently
playing sound, or its next play (in case of a sound asset being
supplied). If the sound is played with looping enabled, subsequent plays
will always start from the beginning (0.0 seconds), *not* from the track
position defined using this function. For example, starting a sound loop
at 5.7 seconds will play the first sound from that point, however after
that it will continue to repeat the whole track, from the beginning to
the end.

#### Syntax:

``` gml
audio_sound_set_track_position(index, time);
```

|          |                                                                                                                                                                                    |                                                                                                                |
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Argument | Type                                                                                                                                                                               | Description                                                                                                    |
| index    |  [Sound Asset](../../../../../The_Asset_Editors/Sounds) or [Sound Instance ID](../../../../../GameMaker_Language/GML_Reference/Asset_Management/Audio/audio_play_sound)    | The index of the sound to change.                                                                              |
| time     |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                                                             | The time (in seconds) to set the start point to. Values longer than the length of the given sound are ignored. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
var snd = audio_play_sound(snd_MainTrack, 0, false);
audio_sound_set_track_position(snd, 32);
```

The above code plays a sound and then uses the returned ID value to set
the start position for the sound to 32 seconds.

# audio_sound_get_track_position

This function will get the position (in seconds) within the sound file
for the sound to play from. The sound can only be a single instance of a
sound (the index for individual sounds being played can be stored in a
variable when using the [ audio_play_sound() ](audio_play_sound) or
[ audio_play_sound_at() ](audio_play_sound_at) functions).

#### Syntax:

``` gml
audio_sound_get_track_position(index);
```

|          |                                                                                                                    |                                                     |
|----------|--------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| Argument | Type                                                                                                               | Description                                         |
| index    |  [Sound Instance ID](../../../../../GameMaker_Language/GML_Reference/Asset_Management/Audio/audio_play_sound)  | The index of the sound to get the play position of. |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
if audio_sound_get_track_position(global.Music) != 0
{
    audio_sound_set_track_position(global.Music, 0);
}
```

The above code checks a track to get it's start position and if it's not
0 seconds it sets it to 0 seconds.

# audio_exists

This function returns whether a sound exists ( true ) or not ( false ).
Note that if the index you search for has not been initialised
previously, this function will cause an error as it is searching for
non-existent asset indices. The sound to check can either be a single
instance of a sound (the index for individual sounds being played can be
stored in a variable when using the [ audio_play_sound()
](audio_play_sound) or [ audio_play_sound_at()
](audio_play_sound_at) functions) or a sound asset.

#### Syntax:

``` gml
audio_exists(index);
```

|          |                                                              |                                                   |
|----------|--------------------------------------------------------------|---------------------------------------------------|
| Argument | Type                                                         | Description                                       |
| index    |  [Sound Asset](../../../../../The_Asset_Editors/Sounds)  | The index of the sound to check the existence of. |

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
if audio_exists(global.Music)
{
    audio_play_sound(global.Music, 0, true);
}
```

The above code checks to see if a sound exists. If it does it is set to
play in a loop.

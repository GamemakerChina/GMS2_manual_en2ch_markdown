# audio_resume_sound

With this function you can resume any sound that is currently paused
(after using the function [ audio_pause_sound() ](audio_pause_sound)
). The sound can either be a single instance of a sound (the index for
individual sounds being played can be stored in a variable when using
the [ audio_play_sound() ](audio_play_sound) or [
audio_play_sound_at() ](audio_play_sound_at) functions) or a sound
asset, in which case *all* instances of the given sound will be
re-started.

#### Syntax:

``` gml
audio_resume_sound(index);
```

|          |                                                                                                                                                                                    |                                   |
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| Argument | Type                                                                                                                                                                               | Description                       |
| index    |  [Sound Asset](../../../../../The_Asset_Editors/Sounds) or [Sound Instance ID](../../../../../GameMaker_Language/GML_Reference/Asset_Management/Audio/audio_play_sound)    | The index of the sound to resume. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if keyboard_check_pressed(ord("P"))
{
    global.Pause = !global.Pause;
    if global.Pause
    {
        audio_pause_sound(snd_Waterfall);
    }
    else
    {
        audio_resume_sound(snd_Waterfall);
    }
}
```

The above code checks for a press of the keyboard key "P" and if it
detects one it sets the global variable "Pause" to true or false and
then either pauses the sound indexed in the variable "snd_Waterfall" or
it resumes the sound from its paused state.

# audio_system_is_available

This function can be used to check and see if the audio system has been
initialised, or if the audio context is running. On all platforms, this
function will return true immediately after Game Start when the audio
engine is initialised, *except on the **HTML5** target* . On HTML5, the
audio context status can change at any time depending on user input, the
browser being used, and its version, so this function can be used to
check and see if audio can be played or not. If the function returns
false (ie: the audio context status is not running), then only
unstreamed sounds *may* play (but it's not guaranteed, and you should
assume that no audio can be played), while if it returns true then all
audio will play.

#### Syntax:

``` gml
audio_system_is_available();
```

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
if audio_system_is_available()
{
    if audio_is_paused(global.Music)
    {
        audio_resume_sound(global.Music)
    }
    else
    {
        if !audio_is_playing(global.Music)
        {
            global.Music = audio_play_sound(snd_Music, 0, true);
        }
    }
}
else
{
    if audio_is_playing(global.Music)
    {
        audio_pause_sound(global.Music);
    }
}
```

The above code will pause/unpause an audio track depending on whether
the audio system is initialised and available or not.

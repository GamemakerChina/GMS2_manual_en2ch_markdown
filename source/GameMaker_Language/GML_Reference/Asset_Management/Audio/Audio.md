# Audio

GameMaker has a complete audio engine that is based on the \*.ogg ,
\*.mp3 and \*.wav sound formats. Sounds of these types added to the IDE
can then be used in your game using the basic audio functions shown
below. For things more complex than basic sound effects or playing a
single piece of music you can refer to the advanced audio functions
which let you modify how a sound is played. There are also a selection
of more specialised functions dedicated to streaming audio, positioning
audio - to give 3D sound - and grouping audio. **IMPORTANT!** When using
audio on the HTML5 target, you should be aware that not all browsers
support Web Audio and so may not play any sound for your project when
run. You can get a general idea of Web Audio support from the following
link: [Can I Use Web Audio?](https://caniuse.com/#search=WebAudio) . The
following functions are for dealing with audio in the most
straightforward and simple way possible, avoiding the use of emitters
and permitting the user to generate sounds and play music easily as
these sounds are always generated at the *listener position* (see the
section linked below for more details on the *listener* ) and so are
generally not affected by any changes to the *listener* :

-   [audio_exists](audio_exists)
-   [audio_get_name](audio_get_name)
-   [audio_get_type](audio_get_type)
-   [audio_play_sound](audio_play_sound)
-   [audio_play_sound_at](audio_play_sound_at)
-   [audio_pause_sound](audio_pause_sound)
-   [audio_pause_all](audio_pause_all)
-   [audio_resume_sound](audio_resume_sound)
-   [audio_resume_all](audio_resume_all)
-   [audio_stop_sound](audio_stop_sound)
-   [audio_stop_all](audio_stop_all)
-   [audio_is_playing](audio_is_playing)
-   [audio_is_paused](audio_is_paused)
-   [audio_create_stream](audio_create_stream)
-   [audio_destroy_stream](audio_destroy_stream)

The following functions are designed to give more control over how the
audio engine works, and how the sounds played through it will be "heard"
by the listener. As such it is recommended that you have a good working
knowledge of how the rest of the GameMaker audio engine works before
using any of the following functions:

-   [audio_sound_set_track_position](audio_sound_set_track_position)
-   [audio_sound_get_track_position](audio_sound_get_track_position)
-   [audio_sound_set_listener_mask](audio_sound_set_listener_mask)
-   [audio_sound_get_listener_mask](audio_sound_get_listener_mask)
-   [audio_sound_length](audio_sound_length)
-   [audio_sound_pitch](audio_sound_pitch)
-   [audio_sound_get_pitch](audio_sound_get_pitch)
-   [audio_sound_is_playable](audio_sound_is_playable)
-   [audio_falloff_set_model](audio_falloff_set_model)
-   [audio_sound_gain](audio_sound_gain)
-   [audio_sound_get_gain](audio_sound_get_gain)
-   [audio_master_gain](audio_master_gain)
-   [audio_set_master_gain](audio_set_master_gain)
-   [audio_get_master_gain](audio_get_master_gain)
-   [audio_channel_num](audio_channel_num)
-   [audio_debug](audio_debug)

Further advanced functionality, like setting listeners, recording audio,
or synchronising multiple audio tracks over time can all be found from
the sub-sections listed below:

-   [Audio Emitters](Audio_Emitters/Audio_Emitters)
-   [Audio Listeners](Audio_Listeners/Audio_Listeners)
-   [Audio Groups](Audio_Groups/Audio_Groups)
-   [Audio Buffers](Audio_Buffers/Audio_Buffers)
-   [Audio
    Synchronisation](Audio_Synchronisation/Audio_Synchronisation)

## Web Audio

When creating games for the HTML5 target platform, the audio engine
requires **Web Audio** support, and this in turn means that sometimes
your audio won't play when or how you expect it. This is because the Web
Audio context may not be running or may stop running when your game is
being played. What causes this varies greatly between browsers, and even
between different versions of the same browser, and so detecting when
the web audio context status changes is very important, e.g.: to detect
when the context changes and pause/start looping audio like background
music. To help with this issue, GameMaker has two separate ways to
detect the change in Web Audio context status, either using the
following function:

-   [audio_system_is_available](audio_system_is_available)

You may also use the **Asynchronous System Event** , which will be
triggered whenever the Web Audio status changes. In this event you will
get the built in [ async_load
](../../../GML_Overview/Variables/Builtin_Global_Variables/async_load)
DS map populated with the key " event_type " which in turn will hold the
string " audio_system_status " if it is an audio event. When this key
exists, there will also be a further " status " key which will be either
" available " or " unavailable ". Note that this event will be triggered
on *all* platforms, but on everything except HTML5 it will only be
triggered once on Game Start when the audio engine is first initialised.
For more information please see the section:

-   [The Asynchronous System
    Event](../../../../The_Asset_Editors/Object_Properties/Async_Events/System)

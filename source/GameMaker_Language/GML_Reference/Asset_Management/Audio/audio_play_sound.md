# audio_play_sound

With this function you can play any sound resource in your game. You
provide the sound index and assign it a priority, which is then used to
determine how sounds are dealt with when the number of sounds playing is
over the limit set by the function [ audio_channel_num()
](audio_channel_num) . Lower priority sounds will be stopped in
favour of higher priority sounds, and the priority value can be any real
number (the actual value is arbitrary, and can be from 0 to 1 or 0 to
100, as GameMaker will prioritize them the same). Note that when dealing
with priority, the *higher* the number the *higher* the priority, such
that a sound with priority 100 will be favoured over a sound with
priority 1. The final argument is for making the sound loop and setting
it to true will make the sound loop until it is stopped and setting it
to false will play the sound once only. This function will also return a
unique index number for the sound being played which can then be stored
in a variable so that you can then pause it or stop it with the
appropriate functions. This means that if you have multiple instances of
the same sound playing at any one time you can target just one instance
of that sound to deal with using the audio functions.

#### Syntax:

``` gml
audio_play_sound(index, priority, loop);
```

|          |                                                                            |                                         |
|----------|----------------------------------------------------------------------------|-----------------------------------------|
| Argument | Type                                                                       | Description                             |
| index    |  [Sound Asset](../../../../../The_Asset_Editors/Sounds)                | The index of the sound to play.         |
| priority |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)     | Set the channel priority for the sound. |
| loop     |  [Boolean](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | Sets the sound to loop or not.          |

#### Returns:

``` gml
 Sound Instance ID
```

#### Example:

``` gml
if health &amp;lt;= 0
{
    lives -= 1;
    audio_play_sound(snd_PlayerDead, 10, false);
}
```

The above code checks the "health" global variable and if it is less
than or equal to 0, it will remove 1 from the "lives" global variable
and play a sound.

# audio_master_gain

With this function you can set the absolute value for the global volume
of all sounds and music. It is based on a linear scale from 0 (silent)
to any value greater than 0, although normally you'd consider the
maximum volume as 1. Anything over 1 can be used but, depending on the
sound used and the platform being compiled to, you may get distortion or
clipping when the sound is played back. This function will affect the
relative volume of all sounds and music played from within your game.

#### Syntax:

``` gml
audio_master_gain(gain);
```

|          |                                                                         |                                       |
|----------|-------------------------------------------------------------------------|---------------------------------------|
| Argument | Type                                                                    | Description                           |
| gain     |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | Value for the global volume (0 to 1). |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if keyboard_check(vk_up)
{
    if vol &amp;lt; 1 vol += 0.05;
    audio_master_gain(vol);
}
if keyboard_check(vk_down)
{
    if vol &amp;gt; 0 vol -= 0.05;
    audio_master_gain(vol);
}
```

The above code checks for key-presses of the up and down arrow keys,
which then increase or decrease the variable "vol". This variable is
then used to set the global gain of all sound and music in the game.

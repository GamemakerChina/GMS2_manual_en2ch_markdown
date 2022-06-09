# audio_emitter_gain

This function sets the maximum gain (volume) for the sound. The
perceived volume for a sound can change depending on the [fall-off
value](audio_emitter_falloff) and the position it has relative to
the *listener* , but by setting the gain with this function, the full
volume will never exceed the specified gain value. The image below
illustrates how gain affects the volume of the emitter when fall-off is
greater than 0:  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/GML/Reference/Audio/Audio_Gain.png)  
This function will change the volume of the sound while it is being
played as well all subsequent sounds played through the given emitter.
Note that on some platforms you can have a gain of greater than 1,
although a value of 1 is considered "full volume" and anything greater
may introduce audio clipping or distortion. ** NOTE ** the final volume
will also be influenced by the global audio gain that has been set by
the function [ audio_master_gain() ](../audio_master_gain) .

#### Syntax:

``` gml
audio_emitter_gain(emitter, gain);
```

|          |                                                                                                                                         |                                     |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------|
| Argument | Type                                                                                                                                    | Description                         |
| emitter  |  [Audio Emitter ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Audio/Audio_Emitters/audio_emitter_create)  | The index of the emitter to change. |
| gain     |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                               | The maximum gain (default 1).       |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if up
{
    gain += 0.05;
    if gain &amp;gt;= 1 up = false;
}
else
{
    gain += 0.05;
    if gain &amp;lt;= 0 up = true;
}

audio_emitter_gain(s_emit, gain);
```

The above code sets the variable "gain" to different values and then
uses that same variable to set the gain of the emitter indexed in the
variable "s_emit".

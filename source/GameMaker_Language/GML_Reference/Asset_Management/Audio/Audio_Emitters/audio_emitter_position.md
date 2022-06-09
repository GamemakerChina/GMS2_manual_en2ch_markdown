# audio_emitter_position

With this function you can change the position of an audio emitter
within the 3D audio space. The position will affect the sound in
different ways depending on where the *listener* is positioned within
the audio space too (default position is (0, 0, 0). See [
audio_listener_position()
](../Audio_Listeners/audio_listener_position) for more information),
so for example if the emitter position is set to (100, 0, 0) and the
current listener is at (200, 0, 0) the audio streamed from the emitter
will appear to be on the left of the audio field. The image below shows
a visual representation of emitters and their relative positions to the
listener:  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/GML/Reference/Audio/Audio_Emitters.png)  

#### Syntax:

``` gml
audio_emitter_position(emitter, x, y, z);
```

|          |                                                                                                                                         |                                     |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------|
| Argument | Type                                                                                                                                    | Description                         |
| emitter  |  [Audio Emitter ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Audio/Audio_Emitters/audio_emitter_create)  | The index of the emitter to change. |
| x        |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                               | The x position.                     |
| y        |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                               | The y position.                     |
| z        |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                               | The z position.                     |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if speed &amp;gt; 0
{
    audio_emitter_position(s_emit, x, y, 0);
}
```

The above code checks to see if the instance speed is over 0 and if it
is it updates the audio emitter indexed in the variable "s_emit" to the
current x/y position.

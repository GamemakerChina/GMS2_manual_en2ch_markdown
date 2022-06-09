# audio_emitter_pitch

This function can be used to change the pitch of all sounds emitted from
the given emitter. It is a *pitch multiplier* , in that the input value
multiplies the current pitch by that amount, so the default value of 1
is no pitch change, while a value of less than 1 will lower the pitch
and greater than 1 will raise the pitch. It is best to use small
increments for this function as any value under 0 or over 5 may not be
audible anyway. ** NOTE ** If a sound is being looped through the
emitter, the change in pitch will not be detected unless the sound is
stopped and looped again!

#### Syntax:

``` gml
audio_emitter_pitch(emitter, pitch);
```

|          |                                                                                                                                         |                                     |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------|
| Argument | Type                                                                                                                                    | Description                         |
| emitter  |  [Audio Emitter ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Audio/Audio_Emitters/audio_emitter_create)  | The index of the emitter to change. |
| pitch    |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                               | The pitch multiplier (default 1).   |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
switch (gear)
{
    case 1: audio_emitter_pitch(s_emit, 0.8); break;
    case 2: audio_emitter_pitch(s_emit, 0.9); break;
    case 3: audio_emitter_pitch(s_emit, 0.95); break;
    case 4: audio_emitter_pitch(s_emit, 1); break;
    case 5: audio_emitter_pitch(s_emit, 1.2); break;
}
```

The above code will change the pitch of the audio played from the
emitter indexed in the variable "s_emit" based on the value of the
variable "gear".

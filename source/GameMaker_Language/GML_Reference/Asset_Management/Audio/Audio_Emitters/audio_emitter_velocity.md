# audio_emitter_velocity

This function can be used to give an emitter *Doppler* effects and
simulate audio motion based on the vector that is resolved from the
given relative x, y and z positions. If the emitter itself is not ever
going to move you would normally not need to set these values, but, for
example, if you are making a scrolling shooter game where the enemies
come from the right and scroll to the left, you would set this to have a
velocity of (hspeed, 0, 0) in the create event of the enemies (and
update the emitter of each instance in the step event using [
audio_emitter_position() ](audio_emitter_position) ) to give any
sounds emitted by the enemy instances the correct Doppler as they pass
the player instance (which in turn would be using the function [
audio_listener_position()
](../Audio_Listeners/audio_listener_position) to set the *listener*
to the correct position).

#### Syntax:

``` gml
audio_emitter_velocity(emitter, vx, vy, vz);
```

|          |                                                                                                                                         |                                     |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------|
| Argument | Type                                                                                                                                    | Description                         |
| emitter  |  [Audio Emitter ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Audio/Audio_Emitters/audio_emitter_create)  | The index of the emitter to change. |
| vx       |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                               | The x vector value (default 0).     |
| vy       |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                               | The y vector value (default 0).     |
| vz       |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                               | The z vector value (default 0).     |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
s_emit = audio_emitter_create();
audio_emitter_position(s_emit, room_width, 0, 0);
audio_emitter_velocity(s_emit, -5, 0, 0);
```

The above code creates an audio emitter and assigns its index to the
variable "s_emit". This emitter is then placed at a position within the
room and given a velocity of 5 pixels per step along the x axis (it will
Doppler correctly in relation to the listener as if it had a horizontal
speed of 5 pixels per step).

# Audio Emitters

Audio emitters are provided to increase the flexibility of the GameMaker
audio engine, and they permit you to add real time effects to your audio
assets, like pitch and Doppler variations, as well as the ability to
position your sounds within the 3D audio space and give them realistic
motion effects. All these functions are affected by the position of the
*listener* within the audio environment and so will require that you use
the provided functions for changing the listener position, velocity and
orientation too (see - [Audio
Listeners](../Audio_Listeners/Audio_Listeners) ). NOTE When using
audio emitters, you must set a falloff model using
[audio_falloff_set_model()](../audio_falloff_set_model) , otherwise
there will be no audio falloff. The following functions exist to deal
with audio emitters:

-   [audio_emitter_create](audio_emitter_create)
-   [audio_emitter_exists](audio_emitter_exists)
-   [audio_emitter_position](audio_emitter_position)
-   [audio_emitter_velocity](audio_emitter_velocity)
-   [audio_emitter_falloff](audio_emitter_falloff)
-   [audio_emitter_gain](audio_emitter_gain)
-   [audio_emitter_pitch](audio_emitter_pitch)
-   [audio_emitter_set_listener_mask](audio_emitter_set_listener_mask)
-   [audio_emitter_free](audio_emitter_free)
-   [audio_play_sound_on](audio_play_sound_on)
-   [audio_emitter_get_gain](audio_emitter_get_gain)
-   [audio_emitter_get_pitch](audio_emitter_get_pitch)
-   [audio_emitter_get_x](audio_emitter_get_x)
-   [audio_emitter_get_y](audio_emitter_get_y)
-   [audio_emitter_get_z](audio_emitter_get_z)
-   [audio_emitter_get_vx](audio_emitter_get_vx)
-   [audio_emitter_get_vy](audio_emitter_get_vy)
-   [audio_emitter_get_vz](audio_emitter_get_vz)
-   [audio_emitter_get_listener_mask](audio_emitter_get_listener_mask)

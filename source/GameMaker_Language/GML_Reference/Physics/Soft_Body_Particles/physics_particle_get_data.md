# physics_particle_get_data

This function returns various pieces of information about each particle
in the physics simulation using the given flags checked. The buffer used
must have been created previously using the function [ buffer_create()
](../../Buffers/buffer_create) , and should be of the "grow" type,
with the size being approximately that of the expected return data. The
flags are set using any of the constants given below, and you would use
the [bitwise
*or*](../../../../Additional_Information/Bitwise_Operators) "\|" to
create a single flag value to get the desired information.

|                                                                                                                                                    |                                                                                                |                |
|----------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|----------------|
|  [Physics Particle Data Flag Constant](../../../../../GameMaker_Language/GML_Reference/Physics/Soft_Body_Particles/physics_particle_get_data)  |                                                                                                |                |
| Constant                                                                                                                                           | Description                                                                                    | Data Type      |
|  phy_particle_data_flag_typeflags                                                                                                                  | The flags value for the particle.                                                              | buffer_u32     |
|  phy_particle_data_flag_position                                                                                                                   | The x and y position of the particle.                                                          | 2 x buffer_f32 |
|  phy_particle_data_flag_velocity                                                                                                                   | The horizontal and vertical speed.                                                             | 2 x buffer_f32 |
|  phy_particle_data_flag_colour                                                                                                                     | The colour and alpha value (hexadecimal).                                                      | buffer_f32     |
|  phy_particle_data_flag_category                                                                                                                   | The particle category (as defined when you created the particle or group to which it belongs). | buffer_u32     |

#### Syntax:

``` gml
physics_particle_get_data(buffer, flags)
```

|          |                                                                                                                                                        |                                                                 |
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| Argument | Type                                                                                                                                                   | Description                                                     |
| buffer   |  [Buffer ID](../../../../../GameMaker_Language/GML_Reference/Buffers/buffer_create)                                                                | The (previously created) buffer to use to store the data.       |
| flags    |  [Physics Particle Data Flag Constant](../../../../../GameMaker_Language/GML_Reference/Physics/Soft_Body_Particles/physics_particle_get_data) (s)  | The flags to use to extract data about specific particle types. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
var count = physics_particle_count();
var flags = phy_particle_data_flag_position | phy_particle_data_flag_colour;
if (count &amp;gt; 0)
{
    var buffer = buffer_create(count * 12, buffer_grow, 4);
    physics_particle_get_data(buffer, flags);
    for (var n = 0; n &amp;lt; count; n++;)
    {
        var xx = buffer_read(buffer, buffer_f32);
        var yy = buffer_read(buffer, buffer_f32);
        var argb = buffer_read(buffer, buffer_u32);
        var alpha = (argb &amp;gt;&amp;gt; 24) &amp;amp; 255;
        draw_sprite_ext(sprBlob, 0, xx, yy, 1, 1, 0, c_green, alpha);
    }
    buffer_delete(buffer);
}
```

The above code gets the number of particles and creates a variable with
the data flags to check, then checks to see if there are any particles
in the room. If there are, a buffer is created and then filled with the
particle data, which is checked and used to draw a sprite at the
particle position.

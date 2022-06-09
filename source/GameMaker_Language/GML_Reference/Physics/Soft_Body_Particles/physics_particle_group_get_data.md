# physics_particle_group_get_data

This function returns various pieces of information about a group of
particles in the physics simulation using the given flags checked. The
group index (its ID) is that which was returned by the function [
physics_particle_group_end() ](physics_particle_group_end) , and the
buffer used must have been created previously using the function [
buffer_create() ](../../Buffers/buffer_create) . It should be of the
"grow" type, with the size being approximately that of the expected
return data. The flags themselves are set using the constants given
below, and you would use the [bitwise
*or*](../../../../Additional_Information/Bitwise_Operators) "\|" to
create a single flag value to get the desired information.

|                                    |                                                                                    |                |
|------------------------------------|------------------------------------------------------------------------------------|----------------|
| Constant                           | Description                                                                        | Data Type      |
|  phy_particle_data_flag_typeflags  | The flags value for the particle.                                                  | buffer_u32     |
|  phy_particle_data_flag_position   | The x and y position of the particle.                                              | 2 x buffer_f32 |
|  phy_particle_data_flag_velocity   | The horizontal and vertical speed.                                                 | 2 x buffer_f32 |
|  phy_particle_data_flag_colour     | The colour and alpha value (hexadecimal).                                          | buffer_f32     |
|  phy_particle_data_flag_category   | The particle category (as defined when you created the group to which it belongs). | buffer_u32     |

#### Syntax:

``` gml
physics_particle_group_get_data(group, buffer, flags)
```

|          |                                                                                                                                                        |                                                                  |
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| Argument | Type                                                                                                                                                   | Description                                                      |
| group    |  [Physics Particle Group ID](../../../../../GameMaker_Language/GML_Reference/Physics/Soft_Body_Particles/physics_particle_group_end)               | The group index (ID) of the particle group to get the data from. |
| buffer   |  [Buffer ID](../../../../../GameMaker_Language/GML_Reference/Buffers/buffer_create)                                                                | The (previously created) buffer to use to store the data.        |
| flags    |  [Physics Particle Data Flag Constant](../../../../../GameMaker_Language/GML_Reference/Physics/Soft_Body_Particles/physics_particle_get_data) (s)  | The flags to use to extract data about specific particle types.  |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
var count = physics_particle_group_count(gp);
var flags = phy_particle_data_flag_position | phy_particle_data_flag_colour;
if (count &amp;gt; 0)
{
    var buffer = buffer_create(count * 12, buffer_grow, 4);
    physics_particle_group_get_data(gp, buffer, flags);
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

The above code gets the position and velocity of the every particle in
the group indexed by the variable "gp", stores the buffer data in a
number of variables, and then uses that to draw a sprite at the position
of each particle in the group.

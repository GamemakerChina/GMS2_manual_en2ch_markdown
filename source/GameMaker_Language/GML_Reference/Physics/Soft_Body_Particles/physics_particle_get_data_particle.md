# physics_particle_get_data_particle

This function returns various pieces of information about a single
particle in the physics simulation using the given flags checked. The
particle index (its ID) is that which was returned by the function [
physics_particle_create() ](physics_particle_create) , and the
buffer used must have been created previously using the function [
buffer_create() ](../../Buffers/buffer_create) . It should be of the
"grow" type, with the size being approximately that of the expected
return data. The flags themselves are set using the constants given
below, and you would use the bitwise *or* "\|" to create a single flag
value to get the desired information.

|                                    |                                                                   |                |
|------------------------------------|-------------------------------------------------------------------|----------------|
| Constant                           | Description                                                       | Data Type      |
|  phy_particle_data_flag_typeflags  | The flags value for the particle.                                 | buffer_u32     |
|  phy_particle_data_flag_position   | The x and y position of the particle.                             | 2 x buffer_f32 |
|  phy_particle_data_flag_velocity   | The horizontal and vertical speed.                                | 2 x buffer_f32 |
|  phy_particle_data_flag_colour     | The colour and alpha value (hexadecimal).                         | buffer_f32     |
|  phy_particle_data_flag_category   | The particle category (as defined when you created the particle). | buffer_u32     |

#### Syntax:

``` gml
physics_particle_get_data_particle(ind, buffer, flags)
```

|          |                                                                                                                                                        |                                                                 |
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| Argument | Type                                                                                                                                                   | Description                                                     |
| ind      |  [Physics Particle ID](../../../../../GameMaker_Language/GML_Reference/Physics/Soft_Body_Particles/physics_particle_create)                        | The index (ID) of the particle to get the data from.            |
| buffer   |  [Buffer ID](../../../../../GameMaker_Language/GML_Reference/Buffers/buffer_create)                                                                | The (previously created) buffer to use to store the data.       |
| flags    |  [Physics Particle Data Flag Constant](../../../../../GameMaker_Language/GML_Reference/Physics/Soft_Body_Particles/physics_particle_get_data) (s)  | The flags to use to extract data about specific particle types. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
var part = physics_particle_create(flags, x, y, x_vel, y_vel, c_white, 1, 1)
var flags = phy_particle_data_flag_position | phy_particle_data_flag_velocity;
var buffer = buffer_create(16, buffer_grow, 4);
physics_particle_get_data_particle(part, buffer, flags);
px = buffer_read(buffer, buffer_f32);
py = buffer_read(buffer, buffer_f32);
pvelx = buffer_read(buffer, buffer_f32);
pvely = buffer_read(buffer, buffer_f32);
buffer_delete(buffer);
```

The above code gets the position and velocity of the particle indexed by
the variable "part" and stores the data in a number of variables.

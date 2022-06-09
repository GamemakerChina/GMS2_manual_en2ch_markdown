# physics_particle_set_radius

With this function you can set the radius (in pixels) for the particles
in a physics simulation. This function is *global* in scope, in that it
will change the radius not just for new particles created after the
change, but also for those already present in the simulation.

#### Syntax:

``` gml
physics_particle_set_radius(radius)
```

|          |                                                                         |                                                 |
|----------|-------------------------------------------------------------------------|-------------------------------------------------|
| Argument | Type                                                                    | Description                                     |
| radius   |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The radius (in pixels) of the particle fixture. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
physics_particle_set_radius(15); physics_particle_set_density(0.5);
 physics_particle_set_damping(1);
 physics_particle_set_gravity_scale(1);
```

The above code will set the base properties for all particles in the
simulation.

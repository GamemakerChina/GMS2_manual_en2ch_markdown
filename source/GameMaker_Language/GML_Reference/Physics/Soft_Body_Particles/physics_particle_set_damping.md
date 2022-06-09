# physics_particle_set_damping

With this function you can set the linear damping of particles in the
simulation. Damping is used to reduce the physics simulation velocity of
instances over time, much like air resistance in the real world. This
function is *global* in scope, in that it will change the damping not
just for new particles created after the change, but also for those
already present in the simulation.

#### Syntax:

``` gml
physics_particle_set_damping(damping)
```

|          |                                                                         |                                                           |
|----------|-------------------------------------------------------------------------|-----------------------------------------------------------|
| Argument | Type                                                                    | Description                                               |
| damping  |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The linear damping to be applied to the particle fixture. |

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

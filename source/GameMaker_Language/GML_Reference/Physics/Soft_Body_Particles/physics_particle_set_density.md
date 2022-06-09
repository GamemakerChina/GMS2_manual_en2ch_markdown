# physics_particle_set_density

With this function you can set the density of the particles in a physics
simulation. Setting the density of the particle will have a direct
impact on how much inertia it has as well as how it reacts to
collisions, so if you make a small particle with a high density it will
have a very large mass, but if you define a large particle with a low
density it will have a much smaller mass. This function is *global* in
scope, in that it will change the density not just for new particles
created after the change, but also for those already present in the
simulation.

#### Syntax:

``` gml
physics_particle_set_density(density)
```

|          |                                                                         |                                      |
|----------|-------------------------------------------------------------------------|--------------------------------------|
| Argument | Type                                                                    | Description                          |
| density  |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The density of the particle fixture. |

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

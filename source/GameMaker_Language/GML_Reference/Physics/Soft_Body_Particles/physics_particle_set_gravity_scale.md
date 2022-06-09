# physics_particle_set_gravity_scale

With this function you can set the gravity scale factor for particles in
the physics simulation. The function is designed to help prevent
instability in the physics simulation, especially when using very small
particles which may behave unpredictably (i.e. break conservation of
momentum) in scenarios such as explosions. Slowing these particles down
by reducing gravity scale can stabilize their behaviour. This function
is *global* in scope, in that it will change the gravity scale not just
for new particles created after the change, but also for those already
present in the simulation. **NOTE** : Adjusting the number of update
iterations per step (using the function [
physics_world_update_iterations()
](../The_Physics_World/physics_world_update_iterations) can also
affect the effect of gravity on particles. Larger iteration sizes confer
greater resistance to gravity.

#### Syntax:

``` gml
physics_particle_set_gravity_scale(scale)
```

|          |                                                                         |                                                                |
|----------|-------------------------------------------------------------------------|----------------------------------------------------------------|
| Argument | Type                                                                    | Description                                                    |
| scale    |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The scaling factor to be applied to gravity for all particles. |

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

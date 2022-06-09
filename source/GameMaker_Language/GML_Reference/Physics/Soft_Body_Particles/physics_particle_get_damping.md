# physics_particle_get_damping

With this function you can find out what the current linear damping is
for particles in the physics simulation (you can set this value using [
physics_particle_set_damping() ](physics_particle_set_damping) ).

#### Syntax:

``` gml
physics_particle_get_damping()
```

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
if (physics_particle_get_damping() &amp;lt; 1)
{
    physics_particle_set_damping(physics_particle_get_damping() + 0.01);
}
```

The above code will check the current damping value for all particles in
the system and if it is less than 1 then it will add 0.01 to it.

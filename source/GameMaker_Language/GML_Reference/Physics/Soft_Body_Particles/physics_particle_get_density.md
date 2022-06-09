# physics_particle_get_density

With this function you can find out what the current density is for
particles in the physics simulation (you can set this value using [
physics_particle_set_density() ](physics_particle_set_density) ).

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
if (physics_particle_get_density() &amp;lt; 1)
{
    physics_particle_set_density(physics_particle_get_density() + 0.01);
}
```

The above code will check the current density value for all particles in
the system and if it is less than 1 then it will add 0.01 to it.

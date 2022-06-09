# physics_particle_get_radius

With this function you can find out what the current radius (in pixels)
is for particles in the physics simulation (you can set this value using
[ physics_particle_set_radius() ](physics_particle_set_radius) ).

#### Syntax:

``` gml
physics_particle_get_radius()
```

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
if (physics_particle_get_radius() &amp;lt; 32)
{
    physics_particle_set_radius(physics_particle_get_radius() + 1);
}
```

The above code will check the current radius of the particles in the
simulation and if it is less than 32, then it will increase their size
by 1.

# physics_particle_get_gravity_scale

With this function you can find out what the current gravity scale
factor is for particles in the physics simulation (you can set this
value using [ physics_particle_set_gravity_scale()
](physics_particle_set_gravity_scale) ).

#### Syntax:

``` gml
physics_particle_get_gravity_scale()
```

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
physics_particle_set_gravity_scale(physics_particle_get_gravity_scale() + 0.1);
```

The above code will set the gravity scale.

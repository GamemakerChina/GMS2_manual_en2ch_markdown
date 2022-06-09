# physics_particle_get_max_count

With this function you can find out what the current cap value is on
particles permitted in the physics simulation (you can set this value
using [ physics_particle_set_max_count()
](physics_particle_set_max_count) ).

#### Syntax:

``` gml
physics_particle_get_max_count()
```

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
if (physics_particle_count() &amp;lt; physics_particle_get_max_count())
{
    physics_particle_create(0, x, y, 0, 0, c_white, 1, 1)
}
```

The above code will check to see if there are less than the maximum
number of permitted particles in the room, and if so create one more.

# physics_particle_count

This function will return the number of particles that are active in a
physics enabled room.

#### Syntax:

``` gml
physics_particle_count()
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

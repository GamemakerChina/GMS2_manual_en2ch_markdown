# part_system_destroy

With this function you can destroy a given particles system and remove
it from memory. This should always be called when the system is no
longer needed, like at the end of a room, or in the destroy event of an
instance, otherwise you could end up with particles appearing in later
rooms and no way to remove them as well as a memory leak which will
eventually crash your game. **NOTE** : This function will also destroy
and remove any emitters that may have been created and associated with
the system being destroyed.

#### Syntax:

``` gml
part_system_destroy(ind);
```

|          |                                                                                                                                      |                                              |
|----------|--------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| Argument | Type                                                                                                                                 | Description                                  |
| ind      |  [Particle System ID](../../../../../../GameMaker_Language/GML_Reference/Drawing/Particles/Particle_Systems/part_system_create)  | The index of the particle system to destroy. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if (global.player_hp &amp;lt;= 0)
{
    part_system_destroy(p_sys);
    room_goto_next();
}
```

The above code checks to see if a global variable value is less than or
equal to zero, and if it is then it destroys the particle system
referenced in the given variable and then goes to the next room.

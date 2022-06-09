# part_system_clear

With this function you can clear the indexed system to its default
state, removing all emitters and resetting the depth and position (if
they had been changed). Be careful using this function as if you have
any instance setting or bursting or any other action using an emitter
associated with this system, you will get an error unless you are using
the [ part_emitter_exists()
](../Particle_Emitters/part_emitter_exists) function to check. There
is also no need to call the
[part_emitter_destroy()](../Particle_Emitters/part_emitter_destroy)
function as this is taken care of automatically too. **NOTE** : this
function will clear the visible particles in the room, but it does
**not** clear the particle properties, nor does it remove them from
memory. For that you should use the functions [ part_type_clear()
](../Particle_Types/part_type_clear) and [ part_type_destroy()
](../Particle_Types/part_type_destroy) .

#### Syntax:

``` gml
part_system_clear(ind);
```

|          |                                                                                                                                      |                                            |
|----------|--------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| Argument | Type                                                                                                                                 | Description                                |
| ind      |  [Particle System ID](../../../../../../GameMaker_Language/GML_Reference/Drawing/Particles/Particle_Systems/part_system_create)  | The index of the particle system to clear. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
part_system_clear(global.Sname);
```

The above code will clear the particle system indexed in the global
variable "Sname" to its default state.

# part_system_create_layer

This function will create a new particle system on a given layer. You
give the unique layer ID as returned by the function [ layer_create()
](../../../Asset_Management/Rooms/General_Layer_Functions/layer_create)
or the name of the layer to use as a string - for example
"instance_layer" - and then flag the system as being persistent or not.
If the system is not flagged as persistent then it will be automatically
destroyed at the end of the room it was created in (this is the same as
if you had called the function [ part_system_destroy()
](part_system_destroy) and will also destroy any emitters associated
with the system). However, when flagged as persistent, the system will
be carried to the next room when the room is changed, and if the
following room does *not* have a layer with the same name or depth as
the one assigned, then a new layer will be created for the system that
is persisting across the rooms, and it will be named the same as
original layer. When changing rooms, if there is another layer in the
following rooms with the same name, then the persisted instance will be
assigned to the layer with the that name *regardless of the depth of the
layer* . Finally, if a persisted system moves to a room with a layer at
the same depth as the layer the system was created on, it will *not* be
assigned to this layer, but instead a new layer will be created at the
same depth (with the same name as the original layer). The function will
return a unique ID value for the particle system that should be used in
all further function calls where you need to give a system ID.
**IMPORTANT!** If you flag the particle system as persistent, then it
(and any emitters assigned to it) will need to be cleaned up manually
using the appropriate destroy functions when not in use, otherwise you
risk a memory leak that will negatively impact your final game.

#### Syntax:

``` gml
part_system_create_layer(layer_id, persistent);
```

|            |                                                                                                                                                                                                                  |                                                                                  |
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| Argument   | Type                                                                                                                                                                                                             | Description                                                                      |
| layer      |  [String](../../../../../../GameMaker_Language/GML_Overview/Data_Types) or [Layer ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/General_Layer_Functions/layer_get_id)    | The layer ID (or name) to assign the particle system to (can be any layer type)  |
| persistent |  [Boolean](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                                                                                     | Flag the particle system as persistent (set to true ) or not (set to false )     |

#### Returns:

``` gml
 Particle System ID
```

#### Example:

``` gml
global.p_sys = part_system_create_layer("effects_layer", true);
```

The above code will create a new particle system on the given layer and
flag it as persisting over subsequent rooms. The ID for the particle
system is stored in a global scope variable for future reference.

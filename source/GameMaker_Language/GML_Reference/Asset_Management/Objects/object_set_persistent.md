# object_set_persistent

With this function you can set the persistence of a specific object. A
persistent object is "carried over" from room to room and maintains its
properties at all times (for more information on persistence see the
section on the [Object
Editor](../../../../The_Asset_Editors/Objects) ). Setting the
persistence of the object means that all instances of this object that
are created *after the persistence has been changed* will be created
persistent, while instances that are already in the room may not be
affected. When you create an instance with persistence enabled in a
room, it will be assigned a layer or a depth (depending on which
function you used to create the instance of the object). When the room
is changed, and if the following room does *not* have a layer with the
same name or depth as the one assigned, then a new layer will be created
for the instance that is persisting across the rooms. If you gave a
named layer when the instance was created, then the new layer will also
be named the same as original layer, while if you assigned a depth to
the instance then the new layer will be named " \_layer_XXX ", where
"XXX" is a hex value used to give the layer a unique name. These layers
will be removed from the room on Room End. Another thing to note about
layers and persistent instances is that if you have assigned the
instance a named layer on creation, and there is another layer in the
following rooms with the same name, then the persisted instance will be
assigned to the layer with the same name *regardless of the depth of the
layer* . Finally, if a persisted instance moves to a room with a layer
at the same depth as the instance was created on, it will *not* be
assigned to this layer, but instead a new layer will be created at the
same depth (following the naming convention explained previously).
Please note that this is not an instance function! You can set the
persistent flag of individual instances using the [ persistent
](../Instances/Instance_Variables/persistent) variable and so have
ten instances all flagged as persistent even though the object in
question has the flag set to false in the IDE, and even if you change
the persistent flag of the object to true using this function, all
instances that currently in the room will remain as they were, and only
instances created after calling the function will start with persistent
flagged as true.

#### Syntax:

``` gml
object_set_persistent(index, pers);
```

|          |                                                                            |                                                                                   |
|----------|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| Argument | Type                                                                       | Description                                                                       |
| index    |  [Object Asset](../../../../../The_Asset_Editors/Objects)              | The index of the object to change.                                                |
| pers     |  [Boolean](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | Whether the object should be flagged as persistent ( true ) or not ( false ).     |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if (room == rm_final)
{
    object_set_persistent(obj_Player, false);
}
instance_create_layer(32, 32, "Instances", obj_Player);
```

The above code checks to see in which room the instance is currently in
and if it is in the specified "rm_final" then it sets the persistence of
the object "obj_Player" to false and then creates the instance.

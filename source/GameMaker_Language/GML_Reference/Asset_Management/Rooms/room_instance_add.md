# room_instance_add

With this function you can add an instance into any room other than the
current one and at any position within that room. The function returns
the unique [ id ](../Instances/Instance_Variables/id) of the
instance which can then be used in further function calls to set
properties etc... of that instance, but **only once the game has entered
the specified room** . If you wish to create an instance in the current
room you should be using the function [ instance_create_layer()
](../Instances/instance_create_layer) . Note that calling this
function on a room asset created in the Asset Browser **will permanently
add the instance to the room** , and even calling game_restart() will
not return the room to it's original state (only ending the game and
opening it again will start with the room in its original state again).

#### Syntax:

``` gml
room_instance_add(index, x, y, obj);
```

|          |                                                                         |                                                     |
|----------|-------------------------------------------------------------------------|-----------------------------------------------------|
| Argument | Type                                                                    | Description                                         |
| index    |  [Room Asset](../../../../../The_Asset_Editors/Rooms)               | The index of the room to add an object instance to. |
| x        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The x position of the new instance.                 |
| y        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The y position of the new instance.                 |
| obj      |  [Object Asset](../../../../../The_Asset_Editors/Objects)           | The object to add an instance of.                   |

#### Returns:

``` gml
 Instance ID
```

#### Example:

``` gml
global.rm = room_add();
room_assign(rm_Base, global.rm);
room_instance_add(global.rm, 100, 100, obj_Player);
```

The above code will add a new room to the game and then copy the
contents of the room indexed as "rm_Base" into it. It will then add an
instance of the object "obj_player" at the position 100,100 of this new
room.

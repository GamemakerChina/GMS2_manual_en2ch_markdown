# skeleton_find_slot

With this function you can find which slots are at a specified
room-space position in the Spine sprite associated with the current
instance. You create a [DS
list](../../../../Data_Structures/DS_Lists/DS_Lists) and supply its
ID along with an x/y position to check and the list will be populated
with name string for each of the available attachment slots for the
sprite (including any attachment modifications). Note that the list is
always sorted in descending order starting from the top-most slot.

#### Syntax:

``` gml
skeleton_find_slot(x, y, list);
```

|          |                                                                                                                   |                                                     |
|----------|-------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| Argument | Type                                                                                                              | Description                                         |
| x        |  [Real](../../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                      | The x position in the room to check.                |
| y        |  [Real](../../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                      | The y position in the room to check.                |
| list     |  [DS List ID](../../../../../../../GameMaker_Language/GML_Reference/Data_Structures/DS_Lists/ds_list_create)  | The ID of the DS list to populate with the DS maps. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
slot_list = ds_list_create();
skeleton_find_slot(mouse_x, mouse_y, slot_list);
```

The above code creates a DS list and then populates it with the slot
names found at the position of the mouse in the room.

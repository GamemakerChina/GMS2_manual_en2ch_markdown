# room_assign

This function will copy one room to another, removing all instances,
tiles etc... from the room that is being copied to and replacing them
completely with the new room contents. You supply the index to for the
room to be copied to (either as defined in the asset browser or as
returned by the function [ room_add() ](room_add) ) as well as the
index of the source room. Note that calling this function on a room
asset created in the Asset Browser **will permanently change the
contents of the room** , and even calling game_restart() will not return
the room to it's original state (only ending the game and opening it
again will start with the room in its original state again).

#### Syntax:

``` gml
room_assign(ind, source);
```

|          |                                                            |                                             |
|----------|------------------------------------------------------------|---------------------------------------------|
| Argument | Type                                                       | Description                                 |
| ind      |  [Room Asset](../../../../../The_Asset_Editors/Rooms)  | The index of the room to be *copied to* .   |
| source   |  [Room Asset](../../../../../The_Asset_Editors/Rooms)  | The index of the room to be *copied from* . |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
global.rm = room_add();
room_assign(global.rm, rm_Base);
```

The above code will add a new room to the game and then copy the
contents of the room indexed as "rm_Base" into it.

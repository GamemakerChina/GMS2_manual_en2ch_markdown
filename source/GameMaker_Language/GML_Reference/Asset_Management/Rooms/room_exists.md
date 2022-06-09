# room_exists

With this function you can check and see whether the room you specify
exists or not. This function takes the room *index* (a real number) and
**not** the room name (a string). This function is most useful when you
are creating rooms dynamically using the function [ room_add()
](room_add) , but you can also use the **read only** variables [
room_first ](room_first) and [ room_last ](room_last) or the
functions [ room_next() ](room_next) and [ room_previous()
](room_previous) to get a specific room index, or provide a variable
that has stored the index of any other room in your game.

#### Syntax:

``` gml
room_exists(index);
```

|          |                                                            |                                 |
|----------|------------------------------------------------------------|---------------------------------|
| Argument | Type                                                       | Description                     |
| index    |  [Room Asset](../../../../../The_Asset_Editors/Rooms)  | The index of the room to check. |

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
if room_exists(global.rm[0])
{
    room_goto(global.rm[0]);
}
```

The above code checks to see if the room indexed in the array
"global.rm\[\]" exists and if it does it then goes to that room.

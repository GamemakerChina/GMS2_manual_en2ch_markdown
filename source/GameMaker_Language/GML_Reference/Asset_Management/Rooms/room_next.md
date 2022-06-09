# room_next

With this function you can retrieve the index of the room *after* the
room input into the function. For example you can use the variable [
room ](room) to get the index of the current room and then use this
function to find the room that follows it, as listed in the [Room
Manager](../../../../Settings/The_Room_Manager) . If there is no
room after the one you input then -1 is returned. Note that this
function will not recognise or take into consideration rooms that have
been added dynamically using [room_add()](room_add) or
[room_duplicate()](room_duplicate) .

#### Syntax:

``` gml
room_next(numb);
```

|          |                                                                         |                                                  |
|----------|-------------------------------------------------------------------------|--------------------------------------------------|
| Argument | Type                                                                    | Description                                      |
| numb     |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The index of the room to get the next one after. |

#### Returns:

``` gml
 Room Asset
```

#### Example:

``` gml
if room_next(room) != -1
{
    room_goto_next();
}
```

The above code will check to see if the next room exists and if so, it
will go to it.

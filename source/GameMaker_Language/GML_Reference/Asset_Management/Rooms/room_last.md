# room_last

This **read only** variable returns the index of the very last room in
the game (this is defined by the order in which the rooms appear in the
[Room Manager](../../../../Settings/The_Room_Manager) and *not* by
the order in which they were created). Note that this variable will not
recognise or take into consideration rooms that have been added
dynamically using [room_add()](room_add) or
[room_duplicate()](room_duplicate) .

#### Syntax:

``` gml
room_last;
```

#### Returns:

``` gml
 Room Asset
```

#### Example:

``` gml
if keyboard_check_pressed(ord("Q"))
{
    room_goto(room_last);
}
```

The above code checks to see if a key has been pressed and if so it goes
to the last room in the game.

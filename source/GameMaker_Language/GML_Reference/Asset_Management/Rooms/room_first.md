# room_first

This **read only** variable returns the index of the very first room in
the game (this is defined by the order in which the rooms appear in the
[Room Manager](../../../../Settings/The_Room_Manager) and *not* by
the order in which they were created).

#### Syntax:

``` gml
room_first;
```

#### Returns:

``` gml
 Room Asset
```

#### Example:

``` gml
if lives &amp;lt; 1
{
    room_goto(room_first);
}
```

The above code will check the "lives" variable and if it is less than 1
go to the first room in the game.

# room_goto_next

With this function you can make your game go to the next one as listed
in the [Room Manager](../../../../Settings/The_Room_Manager) at the
time the game was compiled. If this room does not exist, an error will
be thrown and the game will be forced to close. Note that the room will
not change until the end of the event where the function was called, so
any code after this has been called will still run if in the same event.
NOTE You will not be able to create new instances in the same event
after this function has been called.

#### Syntax:

``` gml
room_goto_next();
```

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if room_exists(room_next(room))
{
    room_goto_next();
}
```

The above code will check to see if there is another room after the
current one and if so it will go to that room.

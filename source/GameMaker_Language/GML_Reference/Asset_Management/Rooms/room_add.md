# room_add

This function will create a new, empty, room and add it to your game,
returning its index to be stored in a variable for all further codes
that deal with this room. Note that each room is permanently added to
the game until the executable is closed, ie: *rooms added through code
cannot be deleted again* . This has important implications for memory
use and so you should use this function with care. **NOTE** : New rooms
are not part of usual room ordering, so they do not have a "previous" or
"next" room (meaning that the functions [ room_next() ](room_next)
and [ room_previous() ](room_previous) will not work). To jump from
the added room to another, you must use the index of the room itself.

#### Syntax:

``` gml
room_add();
```

#### Returns:

``` gml
 Room Asset
```

#### Example:

``` gml
global.myroom = room_add();
room_set_width(global.myroom, 640);
room_set_height(global.myroom, 480);
room_set_persistent(global.myroom, false);
```

This will create a new room and store its index in the variable
"global.myroom". It will then set its width to 640 pixels, its height to
480 pixels, and its persistence to false .

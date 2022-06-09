# room_get_name

This function can be used to return the name of the specified room as a
string. Please note that this is *only* a string and cannot be used to
reference the room directly - for that you would need the *room index* .
You can, however, use this string to get the *room index* using the
returned string along with the function [ asset_get_index()
](../Assets_And_Tags/asset_get_index) .

#### Syntax:

``` gml
room_get_name(index);
```

|          |                                                            |                                             |
|----------|------------------------------------------------------------|---------------------------------------------|
| Argument | Type                                                       | Description                                 |
| index    |  [Room Asset](../../../../../The_Asset_Editors/Rooms)  | The index of the room to check the name of. |

#### Returns:

``` gml
 String
```

#### Example:

``` gml
var roomname = room_get_name(room);

draw_text(32, 32, roomname);
```

The above code will get the name of the current room and draw it on the
screen.

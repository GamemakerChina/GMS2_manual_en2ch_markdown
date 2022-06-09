# room_set_width

With this function you can change (or set) the width of any room in your
game *except the current one* .

#### Syntax:

``` gml
room_set_width(index, w);
```

|          |                                                                         |                                            |
|----------|-------------------------------------------------------------------------|--------------------------------------------|
| Argument | Type                                                                    | Description                                |
| index    |  [Room Asset](../../../../../The_Asset_Editors/Rooms)               | The index of the room to set the width of. |
| w        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The new width of the room in pixels.       |

#### Returns:

``` gml
N/A
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
480 pixels, its caption to 'Game Room' and its persistence to 'false'.

# room_set_view_enabled

With this function you can enable ( true ) or disable ( false ) the view
of any room within your game *except the current one* .

#### Syntax:

``` gml
room_set_view_enabled(index, val);
```

|          |                                                                            |                                                                              |
|----------|----------------------------------------------------------------------------|------------------------------------------------------------------------------|
| Argument | Type                                                                       | Description                                                                  |
| index    |  [Room Asset](../../../../../The_Asset_Editors/Rooms)                  | The index of the room to set.                                                |
| val      |  [Boolean](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | Whether to enable ( true ) or disable ( false ) views in the given room.     |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
global.myroom = room_add();
room_set_view_enabled(global.myroom, true);
```

This will enable views in the room indexed in "global.myroom".

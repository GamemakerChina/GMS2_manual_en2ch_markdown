# room_get_camera

With this function you can get the unique index ID of the camera
assigned to a specific view in a room other than the current one. You
give the room to use, the view port to use (from 0 to 7) and the
function will return a camera index.

#### Syntax:

``` gml
room_get_camera(rm, vind);
```

|          |                                                                         |                                                 |
|----------|-------------------------------------------------------------------------|-------------------------------------------------|
| Argument | Type                                                                    | Description                                     |
| rm       |  [Room Asset](../../../../../The_Asset_Editors/Rooms)               | The index of the room to get the view camera of |
| vind     |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The index of the view port to get the camera of |

#### Returns:

``` gml
 Camera ID
```

#### Example:

``` gml
var cam = room_get_camera(rm_Game, 0);
if cam != global.MainCam
{
    room_set_camera(rm_Game, 0, global.MainCam);
}
```

The above code assigns a camera in a newly created room to view port
\[0\].

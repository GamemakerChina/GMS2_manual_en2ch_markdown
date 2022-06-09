# room_get_viewport

With this function you can retrieve the details of a view port in a room
other than the current one. You give the room ID and the index of the
view port to retrieve (from 0 to 7) and the function will return an
[array](../../../GML_Overview/Arrays) of 5 indices, where:

-   \[0\] = visible (Boolean: true / false )
-   \[1\] = x position (real)
-   \[2\] = y position (real)
-   \[3\] = width (real)
-   \[4\] = height (real)

#### Syntax:

``` gml
room_get_viewport(rm, vind);
```

|          |                                                                         |                                                 |
|----------|-------------------------------------------------------------------------|-------------------------------------------------|
| Argument | Type                                                                    | Description                                     |
| rm       |  [Room Asset](../../../../../The_Asset_Editors/Rooms)               | The index of the room to get viewport data from |
| vind     |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The index of the view port to get               |

#### Returns:

``` gml
 Array

(5 elements: visible, x, y, width, height)
```

#### Example:

``` gml
v_vals = room_get_viewport(rm_Game, 0);

if v_vals[0] == false
{
    room_set_view(rm_Game, true, v_vals[1], v_vals[2], v_vals[3], v_vals[4]);
}
```

The above code retrieves the view port data for the given room then
checks to see if the port is flagged as visible. If it is not, the view
port data is set to make it visible.

# skeleton_bone_state_get

Your skeletal animation is made up of a number of "bones", which you
will have defined and given names to in your animation program, and this
function can be used to get certain data for the named bone at any time.
Note that this data refers to the **current** pose for the skeleton,
depending on the animation set used, and the function requires a
previously created [DS
map](../../../../Data_Structures/DS_Maps/DS_Maps) , which will then
have the following keys and their equivalent values after calling the
function:

-   **"x":** The local x position of the bone relative to the parent
    bone.
-   **"y":** The local y position of the bone relative to the parent
    bone.
-   **"angle":** The local rotation of the bone relative to the parent
    bone.
-   **"xscale":** The local horizontal scale of the bone, in reference
    to the parent bone.
-   **"yscale":** The local vertical scale of the bone, in reference to
    the parent bone.
-   **"worldScaleX":** The magnitude (always positive) of the world
    scale X (this is a *read only* value).
-   **"worldScaleY":** The magnitude (always positive) of the world
    scale Y (this is a *read only* value).
-   **"worldAngleX":** The world rotation for the X axis (this is a
    *read only* value).
-   **"worldAngleY":** The world rotation for the Y axis (this is a
    *read only* value).
-   **"worldX":** The world X position (this is a *read only* value).
-   **"worldY":** The world Y position (this is a *read only* value).
-   **"appliedAngle":** This is the local rotation used to pose the
    skeleton bones.
-   **"parent":** The name (a string) of the parent bone.

The map data returned is similar to that returned for the default pose
when you use [ skeleton_bone_data_get() ](skeleton_bone_state_get) ,
only now you have the extra "world" keys. These refer to the position of
the bone relative to the *root* (origin) of the skeletal animation
sprite, and the returned values do not take into consideration any
scaling or rotation that has been done by setting the built-in sprite
variables like image_xscale or image_angle . The world values are *read
only* and cannot be set. This function is provided so that you can
"intercept" animation data and modify it before it is drawn on the
screen, and as such you would want to use it in the [Other - Animation
Update](../../../../../../The_Asset_Editors/Object_Properties/Other_Events)
event, since this event is triggered just before the Draw Events.

#### Syntax:

``` gml
skeleton_bone_state_get(bone, map);
```

|          |                                                                                                                |                                                            |
|----------|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| Argument | Type                                                                                                           | Description                                                |
| bone     |  [String](../../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                 | The name (as a string) of the bone.                        |
| map      |  [DS Map ID](../../../../../../../GameMaker_Language/GML_Reference/Data_Structures/DS_Maps/ds_map_create)  | The (previously created) DS map that stores the bone data. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
var map = ds_map_create();
skeleton_bone_state_get("head", map);
var xx = ds_map_find_value(map, "worldX");
var yy = ds_map_find_value(map, "worldY");
var deltax = mouse_x - (x + xx);
var deltay = mouse_y - (y + yy);
var angle = -radtodeg(arctan2(deltay, deltax));
ds_map_replace(map, "angle", angle);
skeleton_bone_state_set("head", map);
ds_map_destroy(map);
```

The above code creates a DS map and then populates it with the data from
the bone named "head". It then extracts the world position for the bone,
and uses that data to set the "angle" of the bone to track the mouse
position in the game.

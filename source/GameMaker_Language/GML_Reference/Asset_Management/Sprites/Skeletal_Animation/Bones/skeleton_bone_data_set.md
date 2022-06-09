# skeleton_bone_data_set

Your skeletal animation is made up of a number of "bones", which you
will have defined and given names to in your animation program, and this
function can be used to set certain data for the named bone at any time.
Note that this data refers to the **default** pose for the skeleton, and
*not* the current pose that is being drawn (for that use the function [
skeleton_bone_state_set() ](skeleton_bone_state_set) ), and must be
set from a previously created [DS
map](../../../../Data_Structures/DS_Maps/DS_Maps) , which should
have the following keys and their equivalent values:

-   **"x":** The local x position of the bone relative to the parent
    bone.
-   **"y":** The local y position of the bone relative to the parent
    bone.
-   **"angle":** The local rotation of the bone relative to the parent
    bone.
-   **"xscale":** The local horizontal scale of the bone.
-   **"yscale":** The local vertical scale of the bone.
-   **"parent":** The name (a string) of the parent bone.

#### Syntax:

``` gml
skeleton_bone_data_set(bone, map);
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
var bone_map = ds_map_create();
skeleton_bone_data_get("head", bone_map);
ds_map_replace(bone_map, "parent", "body");
skeleton_bone_data_set("head", bone_map);
ds_map_destroy(bone_map);
```

The above code creates a DS map and then populates it with the data from
the bone named "head". It then replaces the "parent" bone key in the map
with a new value and sets the "head" bone again with the new set of
data.

# tag_get_asset_ids

With this function you can get all the assets of a given type that have
the given tags assigned to them. You supply either a single tag (as a
string) or an array, where each item in the array is a tag (as a
string), as well as the type of asset to check. the type of asset should
be one of the following constants:

|                        |                                                                                                     |
|------------------------|-----------------------------------------------------------------------------------------------------|
| Constant               | Description                                                                                         |
|  asset_object          | The given name refers to an [object](../../../../The_Asset_Editors/Objects) .                   |
|  asset_sprite          | The given name refers to a [sprite](../../../../The_Asset_Editors/Sprites) .                    |
|  asset_sound           | The given name refers to a [sound](../../../../The_Asset_Editors/Sounds) .                      |
|  asset_room            | The given name refers to a [room](../../../../The_Asset_Editors/Rooms) .                        |
|  asset_tiles           | The given name refers to a [tile set](../../../../The_Asset_Editors/Tile_Sets) .                |
|  asset_path            | The given name refers to a [path](../../../../The_Asset_Editors/Paths) .                        |
|  asset_script          | The given name refers to a [script](../../../../The_Asset_Editors/Scripts) .                    |
|  asset_font            | The given name refers to a [font](../../../../The_Asset_Editors/Fonts) .                        |
|  asset_timeline        | The given name refers to a [time line](../../../../The_Asset_Editors/Timelines) .               |
|  asset_shader          | The given name refers to a [shader](../../../../The_Asset_Editors/Shaders) .                    |
|  asset_animationcurve  | The given name refers to an [Animation Curve](../../../../The_Asset_Editors/Animation_Curves) . |
|  asset_sequence        | The given name refers to a [Sequence](../../../../The_Asset_Editors/Sequences) .                |

The function will return an array, where each item in the array will be
a single asset index value. If there are no assets of the type that have
the given tag(s), an empty array will be returned.

#### Syntax:

``` gml
tag_get_asset_ids(tags, asset_type);
```

|            |                                                                                                                                                              |                                                                |
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| Argument   | Type                                                                                                                                                         | Description                                                    |
| tags       |  [String](../../../../../GameMaker_Language/GML_Overview/Data_Types) or [Array](../../../../../GameMaker_Language/GML_Overview/Arrays) of Strings    | A single asset tag string or an array with various asset tags. |
| asset_type |  [Asset Type Constant](../../../../../GameMaker_Language/GML_Reference/Asset_Management/Assets_And_Tags/asset_get_type)                                  | An asset type constant (listed above)                          |

#### Returns:

``` gml
 Array
```

#### Example:

``` gml
var _paths = tag_get_asset_ids("enemy", asset_path);
var _num = irandom(array_length(_paths) - 1);
path_start(_paths[_num], 1, path_action_reverse, false);
```

The above code uses the tag "enemy" to find all the path assets with
that tag, before choosing one at random and assigning it to the instance
running the code.

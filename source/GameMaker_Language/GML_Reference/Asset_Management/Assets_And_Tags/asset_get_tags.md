# asset_get_tags

With this function you can retrieve all the tags assigned to an asset
from the Asset Browser. You supply either the asset name (as a string)
or it's asset index, and the function will return an
[array](../../../GML_Overview/Arrays) of tags for that asset. If no
tags are found or there is an error (ie: the name string given doesn't
exist) then the returned array will be empty. If you supply an asset
index value, then you will need to supply the optional asset type
argument (a constant), as assets of different types can have the same
index, even though they cannot have the same name. The available asset
types are listed in the table below:

|                      |                                                                                                     |
|----------------------|-----------------------------------------------------------------------------------------------------|
| Constant             | Description                                                                                         |
| asset_object         | The given name refers to an [object](../../../../The_Asset_Editors/Objects) .                   |
| asset_sprite         | The given name refers to a [sprite](../../../../The_Asset_Editors/Sprites) .                    |
| asset_sound          | The given name refers to a [sound](../../../../The_Asset_Editors/Sounds) .                      |
| asset_room           | The given name refers to a [room](../../../../The_Asset_Editors/Rooms) .                        |
| asset_tiles          | The given name refers to a [tile set](../../../../The_Asset_Editors/Tile_Sets) .                |
| asset_path           | The given name refers to a [path](../../../../The_Asset_Editors/Paths) .                        |
| asset_script         | The given name refers to a [script](../../../../The_Asset_Editors/Scripts) .                    |
| asset_font           | The given name refers to a [font](../../../../The_Asset_Editors/Fonts) .                        |
| asset_timeline       | The given name refers to a [time line](../../../../The_Asset_Editors/Timelines) .               |
| asset_shader         | The given name refers to a [shader](../../../../The_Asset_Editors/Shaders) .                    |
| asset_animationcurve | The given name refers to an [Animation Curve](../../../../The_Asset_Editors/Animation_Curves) . |
| asset_sequence       | The given name refers to a [Sequence](../../../../The_Asset_Editors/Sequences) .                |

#### Syntax:

``` gml
asset_get_tags(name_or_index, [asset_type]);
```

|                |                                                                                                                                                |                                                                                                            |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| Argument       | Type                                                                                                                                           | Description                                                                                                |
| name_or_index  |  [String](../../../../../GameMaker_Language/GML_Overview/Data_Types) or [Asset](../../../../../The_Asset_Editors/The_Asset_Editors)    | The name of the asset (a string) or its index.                                                             |
| \[asset_type\] |  [Asset Type Constant](../../../../../GameMaker_Language/GML_Reference/Asset_Management/Assets_And_Tags/asset_get_type)                    | OPTIONAL! The type of asset to get the tags for, only used when supplying an index for the first argument. |

#### Returns:

``` gml
 Array
```

#### Example:

``` gml
my_tags = asset_get_tags(object_get_name(object_index));
```

The above code will retrieve all the tags assigned to the object that
the instance running the code has been created from.

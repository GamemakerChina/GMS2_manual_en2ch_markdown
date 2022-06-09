# asset_clear_tags

With this function you can clear all the tags present on any asset from
the asset browser. You supply either the asset name (as a string) or its
asset index, and if you supply an asset index value, then you will need
to supply the optional asset type argument (a constant), as assets of
different types can have the same index, even though they cannot have
the same name. The available asset types are listed in the table below:

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

If the function succeeds in clearing the tags it will return true
otherwise it will return false .

#### Syntax:

``` gml
asset_clear_tags(name,[asset_type]);
```

|                |                                                                                                                                                |                                                                                                               |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Argument       | Type                                                                                                                                           | Description                                                                                                   |
| name_or_index  |  [String](../../../../../GameMaker_Language/GML_Overview/Data_Types) or [Asset](../../../../../The_Asset_Editors/The_Asset_Editors)    | The name of the asset (a string) or its index value (an integer).                                             |
| \[asset_type\] |  [Asset Type Constant](../../../../../GameMaker_Language/GML_Reference/Asset_Management/Assets_And_Tags/asset_get_type)                    | OPTIONAL! The type of asset to clear the tags from, only used when supplying an index for the first argument. |

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
asset_clear_tags(obj_Enemy_Parent, asset_object);
```

The above code will clear all tags from the given object asset.

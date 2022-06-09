# asset_get_type

With this function you can get the type of asset being referenced from
its name (a string). One of the **constants** listed below will be
returned.

#### Syntax:

``` gml
asset_get_type(name);
```

|          |                                                                           |                                                           |
|----------|---------------------------------------------------------------------------|-----------------------------------------------------------|
| Argument | Type                                                                      | Description                                               |
| name     |  [String](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The name of the game asset to get the type of (a string). |

#### Returns:

``` gml
 Asset Type Constant
```

> |                        |                                                                                                     |
> |------------------------|-----------------------------------------------------------------------------------------------------|
> | Constant               | Description                                                                                         |
> |  asset_object          | The given name refers to an [object](../../../../The_Asset_Editors/Objects) .                   |
> |  asset_sprite          | The given name refers to a [sprite](../../../../The_Asset_Editors/Sprites) .                    |
> |  asset_sound           | The given name refers to a [sound](../../../../The_Asset_Editors/Sounds) .                      |
> |  asset_room            | The given name refers to a [room](../../../../The_Asset_Editors/Rooms) .                        |
> |  asset_tiles           | The given name refers to a [tile set](../../../../The_Asset_Editors/Tile_Sets) .                |
> |  asset_path            | The given name refers to a [path](../../../../The_Asset_Editors/Paths) .                        |
> |  asset_script          | The given name refers to a [script](../../../../The_Asset_Editors/Scripts) .                    |
> |  asset_font            | The given name refers to a [font](../../../../The_Asset_Editors/Fonts) .                        |
> |  asset_timeline        | The given name refers to a [time line](../../../../The_Asset_Editors/Timelines) .               |
> |  asset_shader          | The given name refers to a [shader](../../../../The_Asset_Editors/Shaders) .                    |
> |  asset_animationcurve  | The given name refers to an [Animation Curve](../../../../The_Asset_Editors/Animation_Curves) . |
> |  asset_sequence        | The given name refers to a [Sequence](../../../../The_Asset_Editors/Sequences) .                |
> |  asset_unknown         | The given name refers to an asset that either does not exist, or is not one of the above listed.    |

#### Example:

``` gml
if asset_get_type("pth_Path_" + string(global.Game)) == asset_unknown
{
    show_debug_message("Path doesn't exist!!!");
}
else
{
    path_index = asset_get_index("pth_Path_" + string(global.Game));
}
```

The above code checks a dynamically created asset name to see if the
asset is of the correct type. If it is not, then a debug message will be
shown, otherwise the asset name is used to assign the asset to the
instance.

# tileset_get_name

This function will return the name *as a string* of the specified tile
set asset. This name is the one that has been specified for the tile set
in the Asset Browser of the main GameMaker window. Please note that this
is *only* a string and cannot be used to reference the tile set
directly - for that you would need the *tile set index* . You can,
however, use this string to get the *tile set index* using the returned
string along with the function [ asset_get_index()
](../Assets_And_Tags/asset_get_index) .

#### Syntax:

``` gml
tileset_get_name(index);
```

|          |                                                                    |                                               |
|----------|--------------------------------------------------------------------|-----------------------------------------------|
| Argument | Type                                                               | Description                                   |
| index    |  [Tile Set Asset](../../../../../The_Asset_Editors/Tile_Sets)  | The index of the tile set to get the name of. |

#### Returns

``` gml
 String
```

#### **Example:**

``` gml
var _l = layer_get_id("tilemap_trees");
var _m = layer_tilemap_get_id(_l);
var _t = tilemap_get_tileset(_m);
tileset_name = tileset_get_name(_t);
```

The above code will get the name of the tile set index for the given
layer, storing the return string in the variable tileset_name .

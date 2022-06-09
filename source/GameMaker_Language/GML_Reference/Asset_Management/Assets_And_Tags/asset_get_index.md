# asset_get_index

You can use this function to get the unique identifying index for a game
asset from its name. If the asset is not found, the function will return
a value of -1, otherwise it will return the unique index id for the
asset being checked. This id can then be used in other functions as you
would any other index value, like the [ sprite_index
](../Sprites/Sprite_Instance_Variables/sprite_index) or the [
path_index ](../Paths/Path_Variables/path_index) , for example.
Please note that although this function can be used to reference assets
from strings (see example below) you should always make sure that the
asset exists before using it otherwise you may get errors that will
crash your game.

#### Syntax:

``` gml
asset_get_index(name);
```

|          |                                                                           |                                                            |
|----------|---------------------------------------------------------------------------|------------------------------------------------------------|
| Argument | Type                                                                      | Description                                                |
| name     |  [String](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The name of the game asset to get the index of (a string). |

#### Returns:

``` gml
 Asset

(any asset type)
```

#### Example:

``` gml
var obj = asset_get_index("obj_Enemy_" + string(global.Level));
if obj &amp;gt; -1
{
    instance_create_layer(random(room_width), random(room_height), obj, "Enemy_Layer");
}
```

The above code will get an object index from a string, and if that index
exists, create an instance of the object in the game.

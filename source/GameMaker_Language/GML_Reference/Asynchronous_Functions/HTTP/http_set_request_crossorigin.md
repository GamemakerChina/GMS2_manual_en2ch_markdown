# http_set_request_crossorigin

With this function you can set the cross origin type to use when loading
images from a file. The function is exclusively for the HTML5 platform
and is only useful when loading sprites from a file using the
[sprite_add()](../../Asset_Management/Sprites/Sprite_Manipulation/sprite_add)
function. Note that when set to "use-credentials" you no longer need to
give an absolute path to the sprite being loaded, but instead would give
a *relative* path (as shown in the example below). By default the cross
origin type is set to "anonymous".

#### Syntax:

``` gml
http_set_request_crossorigin(origin_type);
```

|             |                                                                         |                                         |
|-------------|-------------------------------------------------------------------------|-----------------------------------------|
| Argument    | Type                                                                    | Description                             |
| origin_type |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The cross origin type to use (a string) |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if string_lower(http_get_request_crossorigin()) != "use-credentials"
{
    http_set_request_crossorigin("use-credentials");
}
sprite_add("sprites/player_outfit_1.png", 0, false, false, 0, 0);
```

The above code will first check the currently set cross origin type and
if it is not "use-credentials" then it is set to "use-credentials" and
then a sprite is added from a file.

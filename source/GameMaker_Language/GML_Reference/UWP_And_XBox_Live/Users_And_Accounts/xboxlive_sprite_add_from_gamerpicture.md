# xboxlive_sprite_add_from_gamerpicture

With this function you can get the gamer picture for a given user ID
pointer. The function works asynchronously, and will trigger an [Image
Loaded](../../../../The_Asset_Editors/Object_Properties/Async_Events/Image_Loaded)
asynchronous event to inform you that the function is finished (like
with HTML5/URL calls to [ sprite_add()
](../../Asset_Management/Sprites/Sprite_Manipulation/sprite_add) ).
The Asynchronous Image Loaded event will have a DS map stored in the
built in variable [ async_load
](../../../GML_Overview/Variables/Builtin_Global_Variables/async_load)
. The map contains the following information:

-   " **filename** ": The complete path to the file you requested.
-   " **id** ": The ID of the resource that you have loaded. This will
    be the same as the variable that you have assigned the resource to.
-   " **status** ": Returns a value of less than 0 for an error.

**NOTE** : When you dynamically load a sprite into your game at runtime,
you must remember to remove it again using [ sprite_delete()
](../../Asset_Management/Sprites/Sprite_Manipulation/sprite_delete)
when no longer needed, otherwise there is risk of a memory leak which
will slow down and eventually crash your game.

#### Syntax:

``` gml
xboxlive_sprite_add_from_gamerpicture(user_id, imagesize, xorig, yorig);
```

|           |                                                                                                                              |                                                      |
|-----------|------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| Argument  | Type                                                                                                                         | Description                                          |
| user_id   |  [Xbox User ID](../../../../../GameMaker_Language/GML_Reference/UWP_And_XBox_Live/Users_And_Accounts/xboxlive_get_user)  | The user ID (a pointer) to get the gamer picture for |
| imagesize |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                       | Size in pixels of the sprite to be returned          |
| xorig     |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                       | Indicate the x position of the origin in the sprite  |
| yorig     |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                       | Indicate the y position of the origin in the sprite  |

#### Returns:

``` gml
 Async Request ID
```

#### Example:

``` gml
var _a = 0;
var _num = xboxlive_get_user_count();
for (var i = 0; i &amp;lt; _num; ++i;)
{
    var _uid = xboxlive_get_user(i);
    if _uid != pointer_null
    {
        global.UserName[_a] = xboxlive_gamedisplayname_for_user(_uid);
        global.UserScore[_a] = xboxlive_gamerscore_for_user(_uid);
        global.UserRep[_a] = xboxlive_reputation_for_user(_uid);
        global.UserAvatar[_a] = xboxlive_sprite_add_from_gamerpicture(_uid, 256, 0, 0);
        ++a;
    }
}
```

The above code loops through the logged in users and stores their gamer
data in various global arrays.

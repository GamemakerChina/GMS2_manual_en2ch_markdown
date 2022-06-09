# Rooms

Rooms are created in the [Room
Editor](../../../../The_Asset_Editors/Rooms) in GameMaker and are
where everything happens in your game. You must have at least one room
in any game for it to run, but you may need many more depending on the
type of game and how you structure your project. This section has all
the general GML functions and variables related to rooms and for getting
information about them as well as for setting certain properties within
them. The following [global
variables](../../../GML_Overview/Variables/Global_Variables) and
functions can be used for getting basic information about any given
room:

-   [room_first](room_first)
-   [room_last](room_last)
-   [room_next](room_next)
-   [room_previous](room_previous)
-   [room](room)
-   [room_speed](room_speed)
-   [room_height](room_height)
-   [room_width](room_width)
-   [room_persistent](room_persistent)

You can also use the following functions to get the name of the current
room (as defined in the [Asset
Browser](../../../../Introduction/The_Asset_Browser) ) as well as
move between rooms:

-   [room_get_name](room_get_name)
-   [room_goto](room_goto)
-   [room_goto_next](room_goto_next)
-   [room_goto_previous](room_goto_previous)
-   [room_restart](room_restart)

Next, we have a series of functions that can be used to change rooms and
their contents or even create new rooms and add to them. It should be
noted that these functions should *never be run from within the room
that you wish to change* , but rather be run from an instance in another
room first. Also note that if you change any room asset in this way, the
change is **permanent** and will be maintained for the entire duration
of the game, even if you call the room_restart() function (closing and
restarting the game will reset the room properties though).

-   [room_exists](room_exists)
-   [room_add](room_add)
-   [room_duplicate](room_duplicate)
-   [room_assign](room_assign)
-   [room_instance_add](room_instance_add)
-   [room_instance_clear](room_instance_clear)
-   [room_set_height](room_set_height)
-   [room_set_width](room_set_width)
-   [room_set_persistent](room_set_persistent)
-   [room_set_view_enabled](room_set_view_enabled)
-   [room_set_viewport](room_set_viewport)
-   [room_get_viewport](room_get_viewport)
-   [room_set_camera](room_set_camera)
-   [room_get_camera](room_get_camera)

There are also a number of different functions related to creating and
manipulating the different types of elements that can be placed on
layers in the room. These functions are listed in the appropriate
sections for each element type listed below:

-   [General Layer
    Functions](General_Layer_Functions/General_Layer_Functions)
-   [Tile Map Layers](Tile_Map_Layers/Tile_Map_Layers)
-   [Background Layers](Background_Layers/Background_Layers)
-   [Sprite Layers](Sprite_Layers/Sprite_Layers)
-   [Sequence Layers](Sequence_Layers/Sequence_Layers)

An important thing to note when creating room layers is that *you can
have multiple different element types on one layer* . So, for example,
you may have a layer for enemies, and on that layer have the enemy
instances as well as certain sprite assets that are only related to that
enemy. Or you could have a background element with a tile map element to
create the look of a room. This is not permitted in the room editor, but
when creating things dynamically you can do this, which is why functions
like [ layer_get_all_elements()
](General_Layer_Functions/layer_get_all_elements) exist.

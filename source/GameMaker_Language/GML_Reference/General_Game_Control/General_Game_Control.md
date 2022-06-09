# General Game Control

These functions and variables are all related to game specific
functionality, like loading/saving, restarting and so on. The following
[global scope](../../GML_Overview/Variables/Global_Variables)
**built-in** variables are useful for debugging your game - they can be
used as the output to a log file in the case of issues, for example - as
well as for showing the current build ID, etc... to the user:

-   [game_id](game_id)
-   [game_save_id](game_save_id)
-   [game_display_name](game_display_name)
-   [game_project_name](game_project_name)

The following functions are used for general game control:

-   [game_end](game_end)
-   [game_restart](game_restart)
-   [game_load](game_load)
-   [game_load_buffer](game_load_buffer)
-   [game_save](game_save)
-   [game_save_buffer](game_save_buffer)
-   [game_get_speed](game_get_speed)
-   [game_set_speed](game_set_speed)

To help you create and maintain highscores for your games, GameMaker
creates a global high score [array](../../GML_Overview/Arrays) of 10
places which you can access, add to, and change to create your own
custom high score lists without too much fuss. This functionality is
local to the game and works on all platforms, so you can easily store
and maintain a basic high score table using these functions along with
the [File Handling Functions](../File_Handling/File_Handling) . The
following functions exist that deal with the internal high score list.

-   [highscore_add](highscore_add)
-   [highscore_name](highscore_name)
-   [highscore_value](highscore_value)
-   [highscore_clear](highscore_clear)

GameMaker also includes a function for drawing the highscores out on the
screen as a list, however it is very basic and it is recommended that
you use this for debugging more than anything else as making your own
high score table is easy and will give you far more control over how it
is displayed:

-   [draw_highscore](../Drawing/Text/draw_highscore)

Finally, we have a function that permits you to assign a sprite to the
mouse cursor:

-   [cursor_sprite](cursor_sprite)

# Struct Forbidden Variables

When creating a struct, it is possible to use certain built-in variables
as member variable names, for example:

``` gml
mystruct =
{
    object_index : obj_Player,
    speed : 3,
    image_blend : c_red
}
```

However, only local and instance scope built-in variables can be used
this way and assigned values as if they were regular struct member
variables. Using **global** scope built-in variables is forbidden and
will cause issues with your game. Below you can find a full list of
these variables so that you know which ones to avoid. The following
built-in global variables are all available for use in your projects but
cannot be used as struct member variables:

-   [argument\[n\]](Variables/Builtin_Global_Variables/argument)
-   [argument0 ...
    argument15](Variables/Builtin_Global_Variables/argument)
-   [argument_count](Variables/Builtin_Global_Variables/argument_count)
-   [async_load](Variables/Builtin_Global_Variables/async_load)
-   [debug_mode](../GML_Reference/Debugging/debug_mode)
-   [pointer_invalid](Variables/Constants)
-   [pointer_null](Variables/Constants)
-   [undefined](Variables/Constants)
-   [NaN](Variables/Constants)
-   [infinity](Variables/Constants)
-   [true](Variables/Constants)
-   [false](Variables/Constants)
-   [pi](Variables/Constants)
-   [room](../GML_Reference/Asset_Management/Rooms/room)
-   [room_first](../GML_Reference/Asset_Management/Rooms/room_first)
-   [room_last](../GML_Reference/Asset_Management/Rooms/room_last)
-   [room_width](../GML_Reference/Asset_Management/Rooms/room_width)
-   [room_height](../GML_Reference/Asset_Management/Rooms/room_height)
-   [room_persistent](../GML_Reference/Asset_Management/Rooms/room_persistent)
-   [score](Variables/Builtin_Global_Variables/score)
-   [lives](Variables/Builtin_Global_Variables/lives)
-   [health](Variables/Builtin_Global_Variables/health)
-   [game_id](../GML_Reference/General_Game_Control/game_id)
-   [game_display_name](../GML_Reference/General_Game_Control/game_display_name)
-   [game_project_name](../GML_Reference/General_Game_Control/game_project_name)
-   [game_save_id](../GML_Reference/General_Game_Control/game_save_id)
-   [working_directory](../GML_Reference/File_Handling/File_Directories/working_directory)
-   [temp_directory](../GML_Reference/File_Handling/File_Directories/temp_directory)
-   [program_directory](../GML_Reference/File_Handling/File_Directories/program_directory)
-   [instance_count](../GML_Reference/Asset_Management/Instances/instance_count)
-   [instance_id](../GML_Reference/Asset_Management/Instances/instance_id)
-   [view_enabled](../GML_Reference/Cameras_And_Display/Cameras_And_Viewports/view_enabled)
-   [view_current](../GML_Reference/Cameras_And_Display/Cameras_And_Viewports/view_current)
-   [view_visible](../GML_Reference/Cameras_And_Display/Cameras_And_Viewports/view_visible)
-   [view_xport](../GML_Reference/Cameras_And_Display/Cameras_And_Viewports/view_xport)
-   [view_yport](../GML_Reference/Cameras_And_Display/Cameras_And_Viewports/view_yport)
-   [view_wport](../GML_Reference/Cameras_And_Display/Cameras_And_Viewports/view_wport)
-   [view_hport](../GML_Reference/Cameras_And_Display/Cameras_And_Viewports/view_hport)
-   [view_surface_id](../GML_Reference/Cameras_And_Display/Cameras_And_Viewports/view_surface_id)
-   [view_camera](../GML_Reference/Cameras_And_Display/Cameras_And_Viewports/view_camera)
-   [mouse_x](../GML_Reference/Game_Input/Mouse_Input/mouse_x)
-   [mouse_y](../GML_Reference/Game_Input/Mouse_Input/mouse_y)
-   [mouse_button](../GML_Reference/Game_Input/Mouse_Input/mouse_button)
-   [mouse_lastbutton](../GML_Reference/Game_Input/Mouse_Input/mouse_lastbutton)
-   [keyboard_key](../GML_Reference/Game_Input/Keyboard_Input/keyboard_key)
-   [keyboard_lastkey](../GML_Reference/Game_Input/Keyboard_Input/keyboard_lastkey)
-   [keyboard_lastchar](../GML_Reference/Game_Input/Keyboard_Input/keyboard_lastchar)
-   [keyboard_string](../GML_Reference/Game_Input/Keyboard_Input/keyboard_string)
-   [cursor_sprite](../GML_Reference/General_Game_Control/cursor_sprite)
-   [fps](../GML_Reference/Debugging/fps)
-   [fps_real](../GML_Reference/Debugging/fps_real)
-   [current_time](../GML_Reference/Maths_And_Numbers/Date_And_Time/current_time)
-   [current_year](../GML_Reference/Maths_And_Numbers/Date_And_Time/current_year)
-   [current_month](../GML_Reference/Maths_And_Numbers/Date_And_Time/current_month)
-   [current_day](../GML_Reference/Maths_And_Numbers/Date_And_Time/current_day)
-   [current_weekday](../GML_Reference/Maths_And_Numbers/Date_And_Time/current_weekday)
-   [current_hour](../GML_Reference/Maths_And_Numbers/Date_And_Time/current_hour)
-   [current_minute](../GML_Reference/Maths_And_Numbers/Date_And_Time/current_minute)
-   [current_second](../GML_Reference/Maths_And_Numbers/Date_And_Time/current_second)
-   [event_type](../GML_Reference/Asset_Management/Objects/Object_Events/event_type)
-   [event_number](../GML_Reference/Asset_Management/Objects/Object_Events/event_number)
-   [event_object](../GML_Reference/Asset_Management/Objects/Object_Events/event_object)
-   [event_action](../GML_Reference/Asset_Management/Objects/Object_Events/event_action)
-   [application_surface](../GML_Reference/Drawing/Surfaces/application_surface)
-   [font_texture_page_size](../GML_Reference/Asset_Management/Fonts/font_texture_page_size)
-   [os_type](../GML_Reference/OS_And_Compiler/os_type)
-   [os_device](../GML_Reference/OS_And_Compiler/os_device)
-   [os_version](../GML_Reference/OS_And_Compiler/os_version)
-   [os_browser](../GML_Reference/OS_And_Compiler/os_browser)
-   [browser_width](../GML_Reference/Web_And_HTML5/browser_width)
-   [browser_height](../GML_Reference/Web_And_HTML5/browser_height)

Apart from those global variables, there are also a number of
**obsolete** built-in global variables that are unavailable due to the
possibility of them being included in imported legacy products (
GameMaker needs to reserve these variables so it can recognise them on
import and flag them to be updated/removed):

-    gamemaker_registered
-    gamemaker_progamemaker_version
-    error_occurred
-    error_last
-    secure_mode
-    show_score
-    show_lives
-    show_health
-    caption_score
-    caption_lives
-    caption_health
-    game_guid
-    argument_relative
-    room_caption
-    room_speed
-    view_xview
-    view_yview
-    view_wview
-    view_hview
-    view_angle
-    view_hborder
-    view_vborder
-    view_hspeed
-    view_vspeed
-    view_object
-    transition_kind
-    transition_steps
-    background_color
-    background_showcolor
-    background_colour
-    background_showcolour
-    background_visible
-    background_foreground
-    background_index
-    background_x
-    background_y
-    background_width
-    background_height
-    background_htiled
-    background_vtiled
-    background_xscale
-    background_yscale
-    background_hspeed
-    background_vspeed
-    background_blend
-    background_alpha

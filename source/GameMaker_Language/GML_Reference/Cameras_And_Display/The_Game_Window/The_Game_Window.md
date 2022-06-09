# The Game Window

The game you create happens in a window (even when fullscreen), and this
window has a number of properties, like position, size, whether it is
fullscreen, etc... These details are normally set automatically for you
based on the room size and view ports enabled in combination with the
settings from [Game Options](../../../../Settings/Game_Options) for
the target platform, but you can change them during the game using the
functions listed on this page. NOTE These functions are for **Windows**
, **Ubuntu** (Linux), **macOS** and **HTML5** target modules only and
may not work on any other device. The following image illustrates how
some general window functions relate and interact with each other:  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/GML/Reference/Cameras_Display/window_position.png)  
Note that the image above shows the game window drawn in a browser, but
the for the other targets, you can replace the browser with the display,
so a function like window_get_y() will return the position of the top of
the game window relative to the display. The following functions exist
to change and get game window properties:

-   [window_center](../The_Game_Window/window_center)
-   [window_handle](../The_Game_Window/window_handle)
-   [window_get_caption](../The_Game_Window/window_get_caption)
-   [window_get_colour](../The_Game_Window/window_get_colour)
-   [window_get_fullscreen](../The_Game_Window/window_get_fullscreen)
-   [window_get_width](../The_Game_Window/window_get_width)
-   [window_get_height](../The_Game_Window/window_get_height)
-   [window_get_x](../The_Game_Window/window_get_x)
-   [window_get_y](../The_Game_Window/window_get_y)
-   [window_get_cursor](../The_Game_Window/window_get_cursor)
-   [window_get_visible_rects](../The_Game_Window/window_get_visible_rects)
-   [window_mouse_get_x](../The_Game_Window/window_mouse_get_x)
-   [window_mouse_get_y](../The_Game_Window/window_mouse_get_y)
-   [window_mouse_set](../The_Game_Window/window_mouse_set)
-   [window_set_caption](../The_Game_Window/window_set_caption)
-   [window_set_colour](../The_Game_Window/window_set_colour)
-   [window_set_fullscreen](../The_Game_Window/window_set_fullscreen)
-   [window_set_position](../The_Game_Window/window_set_position)
-   [window_set_size](../The_Game_Window/window_set_size)
-   [window_set_rectangle](../The_Game_Window/window_set_rectangle)
-   [window_set_cursor](../The_Game_Window/window_set_cursor)
-   [window_set_min_width](../The_Game_Window/window_set_min_width)
-   [window_set_max_width](../The_Game_Window/window_set_max_width)
-   [window_set_min_height](../The_Game_Window/window_set_min_height)
-   [window_set_max_height](../The_Game_Window/window_set_max_height)
-   [window_has_focus](../The_Game_Window/window_has_focus)
-   [window_device](../The_Game_Window/window_device)
-   [window_view_mouse_get_x](../The_Game_Window/window_view_mouse_get_x)
-   [window_view_mouse_get_y](../The_Game_Window/window_view_mouse_get_y)
-   [window_views_mouse_get_x](../The_Game_Window/window_views_mouse_get_x)
-   [window_views_mouse_get_y](../The_Game_Window/window_views_mouse_get_y)

# Mouse Input

Mouse input is accepted on all platforms (on mobile devices it is
accepted as a single screen touch - if you need to use multi-touch, you
should be using the [device specific
functions](../Device_Input/Device_Input) ) and has a few constants
that are used to specify the buttons being pressed. These constants are
shown in the following table:

|                                                                                                                          |                                                                          |
|--------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
|  [Mouse Button Constant](../../../../../GameMaker_Language/GML_Reference/Game_Input/Mouse_Input/mouse_check_button)  |                                                                          |
| Constant                                                                                                                 | Description                                                              |
| mb_left                                                                                                                  | The left mouse button                                                    |
| mb_middle                                                                                                                | The middle mouse button (this may not be valid for all target platforms) |
| mb_right                                                                                                                 | The right mouse button                                                   |
| mb_side1 \*                                                                                                              | Mouse side button 1                                                      |
| mb_side2 \*                                                                                                              | Mouse side button 2                                                      |
| mb_any                                                                                                                   | Any of the mouse buttons                                                 |
| mb_none                                                                                                                  | No mouse button                                                          |

\* **NOTE** : The **mb_side1** and **mb_side2** buttons are only for use
on Windows, macOS, Ubuntu and HTML5. The following functions exist for
the standard mouse button controls:

-   [mouse_button](mouse_button)
-   [mouse_check_button](mouse_check_button)
-   [mouse_check_button_pressed](mouse_check_button_pressed)
-   [mouse_check_button_released](mouse_check_button_released)
-   [mouse_clear](mouse_clear)
-   [mouse_lastbutton](mouse_lastbutton)
-   [mouse_wheel_up](mouse_wheel_up)
-   [mouse_wheel_down](mouse_wheel_down)
-   [mouse_x](mouse_x)
-   [mouse_y](mouse_y)

Note that there are also a set of window functions related to using the
mouse on desktop targets:

-   [window_mouse_get_x](../../Cameras_And_Display/The_Game_Window/window_mouse_get_x)
-   [window_mouse_get_y](../../Cameras_And_Display/The_Game_Window/window_mouse_get_y)
-   [window_mouse_set](../../Cameras_And_Display/The_Game_Window/window_mouse_set)
-   [window_view_mouse_get_x](../../Cameras_And_Display/The_Game_Window/window_view_mouse_get_x)
-   [window_view_mouse_get_y](../../Cameras_And_Display/The_Game_Window/window_view_mouse_get_y)
-   [window_views_mouse_get_x](../../Cameras_And_Display/The_Game_Window/window_views_mouse_get_x)
-   [window_views_mouse_get_y](../../Cameras_And_Display/The_Game_Window/window_views_mouse_get_y)

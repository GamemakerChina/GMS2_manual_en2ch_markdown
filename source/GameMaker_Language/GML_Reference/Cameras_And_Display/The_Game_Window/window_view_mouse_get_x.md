# window_view_mouse_get_x

This function will return the mouse x position relative to the view
selected. **NOTE** : For regular mouse functions see the section on
[Mouse Input](../../Game_Input/Mouse_Input/Mouse_Input)

#### Syntax:

``` gml
window_view_mouse_get_x( id );
```

|          |                                                                         |                                                      |
|----------|-------------------------------------------------------------------------|------------------------------------------------------|
| Argument | Type                                                                    | Description                                          |
| id       |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The id of the view to compare the mouse position to. |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
if mouse_check_button_pressed(mb_left)
{
    var xx, yy;
    xx = window_view_mouse_get_x(0);
    yy = window_view_mouse_get_y(0);

    if xx &amp;gt; 0 &amp;amp;&amp;amp; xx &amp;lt; 32 &amp;amp;&amp;amp; yy &amp;gt; 0 &amp;amp;&amp;amp; yy &amp;lt; 32
    {
        b_press[0] = true;
    }
}
```

The above code will check for a mouse button being pressed, and if it is
it then gets the mouse position relative to the view\[0\] and compares
it to see if a variable should be set to true.

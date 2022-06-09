# window_set_caption

With this function you can change or set the windows caption for the
room that you are currently in. This caption appears at the top of the
window, beside the game icon, when the game is not in full screen mode.

#### Syntax:

``` gml
window_set_caption(caption);
```

|          |                                                                           |                  |
|----------|---------------------------------------------------------------------------|------------------|
| Argument | Type                                                                      | Description      |
| caption  |  [String](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The new caption. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if window_get_caption() != ""
{
    window_set_caption("");
}
```

The above code will check the windows caption to see if it has text or
not, and if it does it sets it to an empty string so as no caption is
displayed.

# window_get_caption

This function returns the caption of the window (this is the text that
appears on the top of the window, beside its icon) and by default this
shows the caption of the room you're currently in.

#### Syntax:

``` gml
window_get_caption();
```

#### Returns:

``` gml
 String
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

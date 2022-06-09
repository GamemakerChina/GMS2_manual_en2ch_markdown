# display_set_ui_visibility

This function can be used to show or hide the system UI on **Android**
*only* . The function requires you to supply one or more system *flags*
as an integer value. When using more than a single flag, these need to
be merged using the bitwise "or", as shown in the example below. You can
find a list of Android system flags
[here](https://developer.android.com/reference/android/view/Viewl#SYSTEM_UI_FLAG_FULLSCREEN)
.

#### Syntax:

``` gml
display_set_ui_visibility(flags);
```

|          |                                                                      |                                                        |
|----------|----------------------------------------------------------------------|--------------------------------------------------------|
| Argument | Type                                                                 | flags                                                  |
| flags    |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types)  | The Android SYSTEM flags to use (as an integer value). |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
var flags = 1024|4096;
display_set_ui_visibility(flags);
```

The above code will use the Android system flags
"SYSTEM_UI_FLAG_IMMERSIVE_STICKY" and "SYSTEM_UI_FLAG_LAYOUT_FULLSCREEN"
to set the visibility of the display.

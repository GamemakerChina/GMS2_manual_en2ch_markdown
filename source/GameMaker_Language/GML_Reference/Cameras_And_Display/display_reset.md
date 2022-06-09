# display_reset

This function Resets the display settings to the ones that were set when
the game was started, but also allows you to change the current level of
full screen anti-aliasing being used and whether to use vertical
synchronisation. The available anti-aliasing levels are 0,2,4 and 8,
with the default startup value being set to 0, and the default v-sync
setting is false (off). Switching v-sync on may give a smoother gaming
experience but it will also need more processing power and so its impact
must be considered careful before use, and the same goes for the
anti-aliasing where the higher the number the more processing that is
required. Since not all target devices are the same, some may not
support 8x or 4x anti-aliasing for example, and so there is a **read
only** variable available for getting the different levels of AA that
the device running the game can display:

``` gml
display_aa
```

This variable will return an integer value based on the setting of bits
for the different levels. So for only 2xAA, this will report 2, for 2x
and 4x availability it will report 6. For 8 and 4 it will report 12. For
all 3 levels (2,4 and 8) it will report 14.

#### Syntax:

``` gml
display_reset(aa, vsync);
```

|          |                                                                         |                                                              |
|----------|-------------------------------------------------------------------------|--------------------------------------------------------------|
| Argument | Type                                                                    | Description                                                  |
| aa       |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types)     | The level of anti-aliasing filtering (0, 2, 4 or 8).         |
| vsync    |  [Boolean](../../../../GameMaker_Language/GML_Overview/Data_Types)  | Toggle vertical synchronisation to on (true) or off (false). |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
if (display_aa &amp;gt; 12)
{
    display_reset(8, true);
}
```

The above code will set the anti-aliasing level to 8 if supported and
switch v-sync to on.

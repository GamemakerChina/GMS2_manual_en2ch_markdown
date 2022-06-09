# video_enable_loop

This function enables or disables looping for the currently loaded
video. Set the enable argument to true to enable looping, and false to
disable it. By default, looping is disabled.

#### Syntax:

``` gml
video_enable_loop(enable);
```

|          |                                                                            |                                                             |
|----------|----------------------------------------------------------------------------|-------------------------------------------------------------|
| Argument | Type                                                                       | Description                                                 |
| enable   |  [Boolean](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | Whether to enable ( true ) or disable ( false ) looping     |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
video_open("Loading.mp4");
video_enable_loop(true);
```

The above code loads a video and enables looping on it.

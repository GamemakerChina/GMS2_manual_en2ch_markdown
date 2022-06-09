# gpu_set_fog

This function can be used to enable or disable fog drawing. Fog can be
used in 3D games to make instances in the distance look faded or even
invisible, which helps in creating atmosphere as well as masking the
fact that you are not drawing instances that are far away. You set
whether it is enabled ( true ) or disabled ( false ), the colour that
the fog should use for blending, as well as the start and end draw
distances. The distance values are essentially depth values in pixels,
and are relative to the camera's position. For example, a position of 0
is nearest to the camera, and with each increase it gets farther away.
By default, a view's camera is placed at -16000 depth, so if you wanted
the fog to start at depth 0 and end at depth 1000, you would set the
start distance to 16000 and the end distance to 17000. The function can
take four individual arguments (given above), or a single array with the
following structure (the example code below shows this method):

-   \[0\] = enabled toggle (a boolean, either true or false ), default
    false
-   \[1\] = colour (real), default c_black
-   \[2\] = start distance (real), default 0
-   \[3\] = end distance (real), default 1

#### Syntax:

``` gml
gpu_set_fog(enable, colour, start, end);
```

|          |                                                                                                           |                                                                  |
|----------|-----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| Argument | Type                                                                                                      | Description                                                      |
| enable   |  [Boolean](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                 | Enable or disable fog                                            |
| colour   |  [Colour](../../../../../GameMaker_Language/GML_Reference/Drawing/Colour_And_Alpha/Colour_And_Alpha)  | The fog colour                                                   |
| start    |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                    | The distance to start applying fog from (relative to the camera) |
| end      |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                    | The distance to end the fog (relative to the camera)             |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
var fog_a = gpu_get_fog();
fog_a[1] = c_red;
gpu_set_fog(fog_a);
```

The above code gets the current fog settings and then sets the colour
element of the array to c_red before setting the fog again using the
changed array.

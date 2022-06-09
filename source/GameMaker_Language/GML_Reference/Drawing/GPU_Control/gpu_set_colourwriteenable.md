# gpu_set_colourwriteenable

With this function you can switch on or off the colour channels and the
alpha channel for all further drawing. For example, you can use this
function to create alpha-channel only surfaces (switch off the RGB
writing before using the surface), or to create special effects while
drawing to the screen. The default value for each of the components is
true , and can be supplied as either four unique arguments or as a 4
element 1D array with the following elements in it which will be either
true (enabled) or false (disabled):

-   \[0\] = Red channel enabled/disabled
-   \[1\] = Green channel enabled/disabled
-   \[2\] = Blue channel enabled/disabled
-   \[3\] = Alpha channel enabled/disabled

#### Syntax:

``` gml
gpu_set_colorwriteenable(red, green, blue, alpha);
```

|          |                                                                            |                                  |
|----------|----------------------------------------------------------------------------|----------------------------------|
| Argument | Type                                                                       | Description                      |
| red      |  [Boolean](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | Enable/disable the red channel   |
| green    |  [Boolean](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | Enable/disable the green channel |
| blue     |  [Boolean](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | Enable/disable the blue channel  |
| alpha    |  [Boolean](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | Enable/disable the alpha channel |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
var cw = gpu_get_colorwriteenable();
cw[3] = false;
gpu_set_colorwriteenable(cw);
```

The above code gets the current colour write values and then sets the
alpha component to false .

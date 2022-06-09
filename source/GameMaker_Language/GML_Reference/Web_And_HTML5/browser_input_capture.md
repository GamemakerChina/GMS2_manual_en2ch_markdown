# browser_input_capture

With this function you can set whether the browser window should capture
all input (set it to false ) or whether the game should capture the
input (set it to true ). Note that this function is for use with the
HTML5 module only.

#### Syntax:

``` gml
browser_input_capture(enable);
```

|          |                                                                         |                                      |
|----------|-------------------------------------------------------------------------|--------------------------------------|
| Argument | Type                                                                    | Description                          |
| enable   |  [Boolean](../../../../GameMaker_Language/GML_Overview/Data_Types)  | Enable or disable game input capture |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
browser_input_capture(true);
```

The above code sets the game to capture all browser input on the HTML5
target platform.

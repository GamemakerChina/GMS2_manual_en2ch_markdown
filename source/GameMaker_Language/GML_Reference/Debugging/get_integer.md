# get_integer

This creates a pop-up window showing a custom message, with a button
labelled "Ok", and prompts the user to input an integer value. The
function will return the typed in integer, or the default value if
nothing has been entered. ** NOTE ** This function is for **debug use
only** on Desktop targets, but is **deprecated** on all other targets.

#### Syntax:

``` gml
get_integer(str, def);
```

|          |                                                                        |                                           |
|----------|------------------------------------------------------------------------|-------------------------------------------|
| Argument | Type                                                                   | Description                               |
| str      |  [String](../../../../GameMaker_Language/GML_Overview/Data_Types)  | The string to show in the pop-up message. |
| def      |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types)    | The default value in the text box.        |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
global.level = get_integer("Level to test?", 1);
```

The above code will display a message prompting the user to select a
level for testing. The return value will be stored in the global
variable "global.level".

# get_string

This creates a pop-up window showing a standard message, with a button
labelled "Ok", that prompts the user to input a string. The function
will return the input string, *or* the default value if nothing has been
entered. ** NOTE ** This function is for **debug use only** on Desktop
targets, but is **deprecated** on all other targets.

#### Syntax:

``` gml
get_string(str, def);
```

|          |                                                                        |                                           |
|----------|------------------------------------------------------------------------|-------------------------------------------|
| Argument | Type                                                                   | Description                               |
| str      |  [String](../../../../GameMaker_Language/GML_Overview/Data_Types)  | The string to show in the pop-up message. |
| def      |  [String](../../../../GameMaker_Language/GML_Overview/Data_Types)  | The default string in the text box.       |

#### Returns:

``` gml
 String
```

#### Example:

``` gml
global.test_name = get_string("Test highscore name:", "Anonymous");
```

The above code will prompt the user to give a name which will then be
stored in the global variable "test_name". If nothing is entered and the
user just presses "Ok" then the default value, "Anonymous", will be
returned.

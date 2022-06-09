# variable_global_get

With this function you can get the value from a given named global
variable. You supply the name of the global variable to get the value of
*as a string* (see example code below) and the function will return the
value held by the global variable or undefined if the variable does not
exist. **IMPORTANT!** If the global variable you are getting does not
exist then the function will return the keyword undefined and you may
get errors that will stop the game from functioning, so if in doubt use
the function [ variable_global_exists ](variable_global_exists)
first.

#### Syntax:

``` gml
variable_global_get(name);
```

|          |                                                                        |                                                      |
|----------|------------------------------------------------------------------------|------------------------------------------------------|
| Argument | Type                                                                   | Description                                          |
| name     |  [String](../../../../GameMaker_Language/GML_Overview/Data_Types)  | The name of the global variable to get (as a string) |

#### Returns:

``` gml
 Variable

(any data type) or

 undefined

(if the named variable does not exist)
```

#### Example:

``` gml
if variable_global_exists("enemy_num")
{
    show_debug_message("enemy_num = " + string(variable_global_get("enemy_num"));)
}
```

The above code will check to see if a global variable exists and if it
does then it is output to the console.

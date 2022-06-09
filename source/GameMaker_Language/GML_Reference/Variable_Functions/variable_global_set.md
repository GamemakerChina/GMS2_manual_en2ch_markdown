# variable_global_set

With this function you can set the value of a given global variable. You
supply the name of the global variable to set the value of *as a string*
(see example code below), and then the value to set (can be any valid
[data type](../../GML_Overview/Data_Types) ). If the global variable
does not exist already in the game it will be created and then assigned
the value.

#### Syntax:

``` gml
variable_global_set(name, val);
```

|          |                                                                                   |                                                      |
|----------|-----------------------------------------------------------------------------------|------------------------------------------------------|
| Argument | Type                                                                              | Description                                          |
| name     |  [String](../../../../GameMaker_Language/GML_Overview/Data_Types)             | The name of the global variable to set (as a string) |
| val      |  [Variable](../../../../GameMaker_Language/GML_Overview/Data_Types#variable)  | The value to set the global variable to              |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if !variable_global_exists("enemy_num")
{
    variable_global_set("enemy_num", 0);
}
```

The above code will check to see if a global variable exists and if it
does not then it is created and set to 0.

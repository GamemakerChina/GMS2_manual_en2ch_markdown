# variable_global_exists

With this function you can check whether a global scope variable exists
or not. You supply the global variable name to check for *as a string*
(see example code below) and the function will return true if a global
variable with the given name exists or false otherwise.

#### Syntax:

``` gml
variable_global_exists(name);
```

|          |                                                                        |                                                            |
|----------|------------------------------------------------------------------------|------------------------------------------------------------|
| Argument | Type                                                                   | Description                                                |
| name     |  [String](../../../../GameMaker_Language/GML_Overview/Data_Types)  | The name of the global variable to check for (as a string) |

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
if !variable_global_exists("enemy_num")
{
    global.enemy_num = instance_number(obj_Enemey_Parent);
}
```

The above code will check to see if the global variable called
"enemy_num" exists and if it does not it is created and set a value.

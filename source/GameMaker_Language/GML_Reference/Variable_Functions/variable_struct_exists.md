# variable_struct_exists

With this function you can check whether a variable exists within the
given struct or not. You supply the struct reference to use as well as
the variable name to check for *as a string* (see example code below).
The function will return true if a variable with the given name exists
for the struct and false otherwise.

#### Syntax:

``` gml
variable_struct_exists(struct, name);
```

|          |                                                                        |                                                            |
|----------|------------------------------------------------------------------------|------------------------------------------------------------|
| Argument | Type                                                                   | Description                                                |
| struct   |  [Struct](../../../../GameMaker_Language/GML_Overview/Structs)     | The struct reference to check                              |
| name     |  [String](../../../../GameMaker_Language/GML_Overview/Data_Types)  | The name of the struct variable to check for (as a string) |

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
if !variable_struct_exists(mystruct, "shields")
{
    mystruct.shields = 0;
}
```

The above code will check to see if the variable called "shields" exists
in the given struct and if it does not then it is created and
initialised to 0.

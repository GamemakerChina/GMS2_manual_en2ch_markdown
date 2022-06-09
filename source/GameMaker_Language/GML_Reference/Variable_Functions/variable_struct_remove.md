# variable_struct_remove

With this function you can remove a variable from a struct. You supply
the struct ID to remove the variable from and the string name of the
variable to be removed.

#### Syntax:

``` gml
variable_struct_remove(struct, name);
```

|          |                                                                        |                                                  |
|----------|------------------------------------------------------------------------|--------------------------------------------------|
| Argument | Type                                                                   | Description                                      |
| struct   |  [Struct](../../../../GameMaker_Language/GML_Overview/Structs)     | The struct reference to remove the variable from |
| name     |  [String](../../../../GameMaker_Language/GML_Overview/Data_Types)  | The name of the variable to remove (as a string) |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if variable_struct_exists(mystruct, "shields")
{
    variable_struct_remove(mystruct, "shields");
}
```

The above code will check to see if the given variable exists in the
given struct and if it does then it is removed.

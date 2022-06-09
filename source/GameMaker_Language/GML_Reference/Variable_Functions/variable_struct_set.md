# variable_struct_set

With this function you can set the value of a given variable in a
struct. You supply the struct reference as well as the name of the
variable to set the value of *as a string* (see example code below), and
then finally the value to set (can be any valid [data
type](../../GML_Overview/Data_Types) ). If the variable does not
exist already in the struct it will be created and then assigned the
value.

#### Syntax:

``` gml
variable_struct_set(struct, name, val);
```

|          |                                                                                   |                                               |
|----------|-----------------------------------------------------------------------------------|-----------------------------------------------|
| Argument | Type                                                                              | Description                                   |
| struct   |  [Struct](../../../../GameMaker_Language/GML_Overview/Structs)                | The struct reference to set                   |
| name     |  [String](../../../../GameMaker_Language/GML_Overview/Data_Types)             | The name of the variable to set (as a string) |
| val      |  [Variable](../../../../GameMaker_Language/GML_Overview/Data_Types#variable)  | The value to set the variable to              |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if !variable_struct_exists(mystruct, "shields")
{
    variable_struct_set(mystruct, "shields", 0);
}
```

The above code will check to see if the given variable exists in the
given struct and if it does not then it is created and set to 0.

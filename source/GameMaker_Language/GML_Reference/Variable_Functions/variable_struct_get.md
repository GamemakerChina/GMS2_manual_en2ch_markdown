# variable_struct_get

With this function you can get the value from a given named variable
within a struct. You supply the struct reference as well as the name of
the variable to get the value of *as a string* (see example code below).
The function will return the value held by the variable or undefined if
the named variable does not exist. **IMPORTANT!** If the variable you
are getting does not exist then the function will return the keyword
undefined and you may get errors that will stop the game from
functioning, so if in doubt use the function [ variable_struct_exists()
](variable_struct_exists) first.

#### Syntax:

``` gml
variable_struct_get(struct, name);
```

|          |                                                                        |                                               |
|----------|------------------------------------------------------------------------|-----------------------------------------------|
| Argument | Type                                                                   | Description                                   |
| struct   |  [Struct](../../../../GameMaker_Language/GML_Overview/Structs)     | The struct reference to use                   |
| name     |  [String](../../../../GameMaker_Language/GML_Overview/Data_Types)  | The name of the variable to get (as a string) |

#### Returns:

``` gml
 Variable

(any data type) or

 undefined

(if the named variable does not exist)
```

#### Example:

``` gml
if variable_struct_exists(mystruct, "shields")
{
    var ss = variable_struct_get(mystruct, "shields");
}
else
{
    var ss = -1;
}
```

The above code will check to see if a variable exists in the given
struct and if it does then the value it holds is retrieved and stored in
a local variable. If it does not exist, the local variable is set to -1.

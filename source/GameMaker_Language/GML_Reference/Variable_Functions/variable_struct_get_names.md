# variable_struct_get_names

With this function you can retrieve an array populated with the variable
names from a struct. You pass in the struct reference to check, and each
entry in the array will be a **string** of the variable names that the
struct contains.

#### Syntax:

``` gml
variable_struct_get_names(struct);
```

|          |                                                                     |                                |
|----------|---------------------------------------------------------------------|--------------------------------|
| Argument | Type                                                                | Description                    |
| struct   |  [Struct](../../../../GameMaker_Language/GML_Overview/Structs)  | The struct reference to check. |

#### Returns:

``` gml
 Array

(each entry is a string)
```

#### Example:

``` gml
var str = "";
var array = variable_struct_get_names(mystruct);
show_debug_message("Variables for struct: " + string(array));
for (var i = 0; i &amp;lt; array_length(array); i++;)
{
    str = array[i] + ":" + string(variable_struct_get(mystruct, array[i]));
    show_debug_message(str);
}
```

The above code will retrieve an array of the variable names for the
given struct and then display these along with their values in the debug
output.

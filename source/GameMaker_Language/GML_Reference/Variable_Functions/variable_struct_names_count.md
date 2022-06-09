# variable_struct_names_count

With this function you can find the total number number of variables
defined for a struct. You supply the struct ID to check, and the
function will return an integer value for the number of variables
encountered, or (if no struct of the given ID exists) -1.

#### Syntax:

``` gml
variable_struct_names_count(struct_id);
```

|           |                                                                     |                                             |
|-----------|---------------------------------------------------------------------|---------------------------------------------|
| Argument  | Type                                                                | Description                                 |
| struct_id |  [Struct](../../../../GameMaker_Language/GML_Overview/Structs)  | The unique ID value of the struct to check. |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
var _num = variable_struct_names_count(mystruct); show_debug_message("Struct Variables = " + string(_num));
```

The above code will retrieve the number of variables in the given struct
and show a debug message in the console output with this value.

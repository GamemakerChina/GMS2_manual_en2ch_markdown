# is_undefined

This function returns whether a given variable is defined or not. In
some cases you want to check and see what data type a variable holds in
GameMaker and that's when you would use this function. It returns true
or false depending on whether the value is defined or not. **NOTE** :
This function **cannot** be used to verify the existence of a variable.
Use [ variable_instance_exists() ](variable_instance_exists) or [
variable_global_exists() ](variable_global_exists) instead.

#### Syntax:

``` gml
is_undefined(n);
```

|          |                                                                                   |                        |
|----------|-----------------------------------------------------------------------------------|------------------------|
| Argument | Type                                                                              | Description            |
| n        |  [Variable](../../../../GameMaker_Language/GML_Overview/Data_Types#variable)  | The argument to check. |

#### Returns:

``` gml
 Boolean
```

#### **Example:**

``` gml
var val = ds_map_find_value(map, 13);
if is_undefined(val)
{
    show_debug_message("Map entry does not exist!");
}
```

The above code checks the variable "val" to see if it is undefined or
not and shows a debug message if it is.
